---
title: Comparando entradas do Livro de Endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415352"
---
# <a name="comparing-address-book-entries"></a>Comparando entradas do Livro de Endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A implementação de [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) do provedor compara os identificadores de entrada de dois dos objetos do provedor. MAPI calls this method after determining that the two entry identifiers contain your provider's registered [MAPIUID](mapiuid.md). Portanto, seu **método CompareEntryIDs** não precisa verificar se os identificadores de entrada passados para os parâmetros  _lpEntryID1_ e  _lpEntryID2_ pertencem ao seu provedor. 
  
Chamar **IABLogon::CompareEntryIDs** é equivalente **a** recuperar a propriedade PR_RECORD_KEY ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) para cada um dos dois objetos e compará-los diretamente.
  
 **Para implementar CompareEntryIds**
  
1. Verifique o tipo dos identificadores de entrada passados se o provedor armazenar essas informações. Por exemplo, um identificador de entrada pode pertencer a um usuário de mensagens enquanto o outro pode pertencer a uma lista de distribuição. Se os tipos não corresponderem, defina o conteúdo do parâmetro  _lpulResult_ como FALSE e retorne. 
    
2. Compare os tamanhos dos dois identificadores de entrada. Se eles não são os mesmos, defina o conteúdo do parâmetro  _lpulResult_ como FALSE e retorne. 
    
3. Verifique se o tamanho dos identificadores de entrada é o tamanho correto para seu tipo. Se não estiver, defina o conteúdo do parâmetro  _lpulResult_ como FALSE e retorne o valor de erro MAPI_E_UNKNOWN_ENTRYID. 
    
4. Verifique se os identificadores de entrada são os mesmos. Se compararem igualmente, defina o conteúdo do parâmetro  _lpulResult_ como VERDADEIRO e retorne. Caso contrário, de definida como FALSE antes de retornar. 
    
5. Se o provedor estiver comparando um identificador de entrada de curto prazo com um identificador de longo prazo, ele deverá comparar igualmente.
    

