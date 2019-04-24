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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270039"
---
# <a name="linking-to-the-mapi-dlls"></a>Vincular a DLLs MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes MAPI podem vincular as DLLs MAPI implicitamente ou explicitamente usando as funções do Windows **LoadLibrary** e **GetProcAddress**. Para obter informações sobre como vincular DLLs MAPI explicitamente, consulte [link to MAPI Functions](how-to-link-to-mapi-functions.md).
  
MAPI fornece instruções de definição de tipo no MAPIX. Arquivo de cabeçalho H para cada uma das seguintes funções:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Use essas definições de tipo para chamar corretamente os pontos de entrada correspondentes se você vincular explicitamente às DLLs MAPI.
  
Os provedores de serviços podem conter funcionalidade não MAPI, recursos que não são completamente relacionados ao MAPI — em sua DLL. Se você precisar usar esses recursos, chame **LoadLibrary** antes de usar a dll e o **FreeLibrary** para remover a DLL da memória após o uso. Como o MAPI não está ciente de usos não MAPI de uma DLL de provedor de serviços, não há garantia de que a DLL estará disponível quando necessário. O MAPI libera uma DLL de provedor de serviços quando não há mais clientes com sessões ativas que exigem seus serviços. 
  

