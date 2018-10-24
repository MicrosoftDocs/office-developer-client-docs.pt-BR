---
title: Comparar entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e5c46aed7a15ae4f48c8e4f1fe308fcb20ab3fe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575354"
---
# <a name="comparing-address-book-entries"></a>Comparar entradas do catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementação de [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) do seu provedor compara os identificadores de entrada para dois dos objetos do seu provedor. MAPI chama esse método depois determinando se os identificadores de dois entrada contêm seu provedor registrado [MAPIUID](mapiuid.md). Portanto, seu método **CompareEntryIDs** não precisa verificar se os identificadores de entrada passados para os parâmetros _lpEntryID1_ e _lpEntryID2_ pertencem ao seu provedor. 
  
Chamar **IABLogon::CompareEntryIDs** é equivalente a recuperar a propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada um dos dois objetos e compará-los diretamente.
  
 **Para implementar CompareEntryIds**
  
1. Verifique o tipo dos identificadores de entrada passados se seu provedor armazena essas informações. Por exemplo, um identificador de entrada pode pertencer a um usuário de mensagens, enquanto a outra pode pertencer a uma lista de distribuição. Se os tipos não coincidirem, defina o conteúdo do parâmetro _lpulResult_ como FALSE e retorno. 
    
2. Compare os tamanhos dos identificadores de entrada de dois. Se não forem iguais, defina o conteúdo do parâmetro _lpulResult_ como FALSE e retorno. 
    
3. Verifique se o tamanho dos identificadores de entrada é o tamanho correto para seu tipo. Caso contrário, defina o conteúdo do parâmetro _lpulResult_ como FALSE e retornar o valor de erro MAPI_E_UNKNOWN_ENTRYID. 
    
4. Verifique se os identificadores de entrada são os mesmos. Se eles compararem igualmente, defina o conteúdo do parâmetro _lpulResult_ como TRUE e retorno. Caso contrário, defina como FALSE antes de retornar. 
    
5. Se seu provedor está comparando um identificador curto prazo de entrada com um identificador de longo prazo, eles devem compare igualmente.
    

