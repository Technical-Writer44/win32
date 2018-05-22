---
title: Traversing the Heap List
description: The following example obtains a list of heaps for the current process.
ms.assetid: 'cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3'
---

# Traversing the Heap List

The following example obtains a list of heaps for the current process. It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](createtoolhelp32snapshot.md) function, and then walks through the list using the [**Heap32ListFirst**](heap32listfirst.md) and [**Heap32ListNext**](heap32listnext.md) functions. For each heap, it uses the [**Heap32First**](heap32first.md) and [**Heap32Next**](heap32next.md) functions to walk the heap blocks.


```C++
#include <windows.h>
#include <tlhelp32.h>
#include <stdio.h>

int main( void )
{
   HEAPLIST32 hl;
   
   HANDLE hHeapSnap = CreateToolhelp32Snapshot(TH32CS_SNAPHEAPLIST, GetCurrentProcessId());
   
   hl.dwSize = sizeof(HEAPLIST32);
   
   if ( hHeapSnap == INVALID_HANDLE_VALUE )
   {
      printf ("CreateToolhelp32Snapshot failed (%d)\n", GetLastError());
      return 1;
   }
   
   if( Heap32ListFirst( hHeapSnap, &amp;hl ) )
   {
      do
      {
         HEAPENTRY32 he;
         ZeroMemory(&amp;he, sizeof(HEAPENTRY32));
         he.dwSize = sizeof(HEAPENTRY32);

         if( Heap32First( &amp;he, GetCurrentProcessId(), hl.th32HeapID ) )
         {
            printf( "\nHeap ID: %d\n", hl.th32HeapID );
            do
            {
               printf( "Block size: %d\n", he.dwBlockSize );
               
               he.dwSize = sizeof(HEAPENTRY32);
            } while( Heap32Next(&amp;he) );
         }
         hl.dwSize = sizeof(HEAPLIST32);
      } while (Heap32ListNext( hHeapSnap, &amp;hl ));
   }
   else printf ("Cannot list first heap (%d)\n", GetLastError());
   
   CloseHandle(hHeapSnap); 

   return 0;
}
```



 

 



