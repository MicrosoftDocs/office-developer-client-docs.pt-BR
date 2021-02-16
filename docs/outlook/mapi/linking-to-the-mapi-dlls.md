---
title: Vincular a DLLs MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419300"
---
# <a name="linking-to-the-mapi-dlls"></a>Vincular a DLLs MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Clientes MAPI podem vincular as DLLs MAPI implicitamente ou explicitamente usando as funções Windows **LoadLibrary** e **GetProcAddress**. Para obter informações sobre como vincular explicitamente DLLs MAPI, consulte [Link para funções MAPI](how-to-link-to-mapi-functions.md).
  
MAPI provides type definition statements in the MAPIX. Arquivo de header H para cada uma das seguintes funções:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Use essas definições de tipo para chamar corretamente os pontos de entrada correspondentes se você vincular explicitamente às DLLs MAPI.
  
Os provedores de serviços podem conter funcionalidades não MAPI — recursos completamente não relacionados ao MAPI — em sua DLL. Se você precisar usar esses recursos, chame **LoadLibrary** antes de usar a DLL e **o FreeLibrary** para remover a DLL da memória após seu uso. Como o MAPI não está ciente de usos não MAPI de um provedor de serviços DLL, não há garantia de que a DLL estará disponível quando necessário. A MAPI libera uma DLL de provedor de serviços quando não há mais clientes com sessões ativas que exigem seus serviços. 
  

