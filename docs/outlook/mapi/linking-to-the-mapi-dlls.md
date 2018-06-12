---
title: Vinculando a DLLs MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0bce1d682057b81135d1684c40bc79e6710d4e2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767757"
---
# <a name="linking-to-the-mapi-dlls"></a>Vinculando a DLLs MAPI

  
  
**Aplica-se a**: Outlook 
  
Clientes MAPI podem vincular a DLLs MAPI implícita ou explicitamente, usando as funções do Windows **LoadLibrary** e **GetProcAddress**. Para obter informações sobre como vincular explicitamente DLLs MAPI, consulte o [Link para funções de MAPI](how-to-link-to-mapi-functions.md).
  
MAPI fornece instruções de definição de tipo no MAPIX. Arquivo de cabeçalho H para cada uma das seguintes funções:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Use essas definições de tipo para chamar corretamente os pontos de entrada correspondente, se você vincular explicitamente DLLs MAPI.
  
Provedores de serviços podem conter a funcionalidade de não-MAPI — recursos que estão completamente não relacionados à MAPI — em seu DLL. Se você precisar usar estes recursos, chame **LoadLibrary** antes de usar a DLL e **FreeLibrary** para remover a DLL da memória depois usá-las. Como MAPI está ciente dos usos de não-MAPI de um provedor de serviços DLL, não há nenhuma garantia de que a DLL esteja disponível quando necessário. MAPI libera um provedor de serviços DLL quando não existem mais todos os clientes com as sessões ativas que exigem seus serviços. 
  

