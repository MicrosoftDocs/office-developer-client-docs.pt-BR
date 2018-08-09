---
title: Retornar convenção de nomenclatura de valor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 990a48c661621a3a704236a850f5d09239a12fca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770275"
---
# <a name="return-value-naming-convention"></a>Retornar convenção de nomenclatura de valor

  
  
**Aplica-se a**: Outlook 
  
O MAPICODE. Arquivo de cabeçalho H contém muitos dos valores que um provedor de cliente ou serviço pode retornar de uma implementação do método de interface ou pode ver retornado de uma chamada.
  
Os códigos para representar as condições de aviso e de falha siga uma convenção de nomenclatura diferente que começa com o prefixo MAPI, um caractere de sublinhado e um W ou um E para indicar o tipo de código. O restante do código é uma cadeia de caracteres curta para descrever a condição. Cada palavra na cadeia de caracteres é separada por um caractere de sublinhado. Por exemplo, o valor de erro MAPI_E_TOO_COMPLEX indica que a implementação não pôde tratar qualquer item estava sendo solicitado na chamada. O valor de aviso MAPI_W_PARTIAL_COMPLETION indica que a chamada foi bem-sucedida, mas houve problemas. Somente a parte da operação foi concluída com êxito.
  

