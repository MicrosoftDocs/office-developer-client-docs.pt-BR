---
title: Convenção de Nomen por Valor de Retorno
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423612"
---
# <a name="return-value-naming-convention"></a>Convenção de Nomen por Valor de Retorno

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPICODE. O arquivo de header H contém muitos dos valores que um cliente ou provedor de serviços pode retornar de uma implementação de método de interface ou pode ver retornado de uma chamada.
  
Os códigos para representar condições de aviso e falha seguem uma convenção de nomenal diferente que começa com o prefixo MAPI, um sublinhado e um W ou E para indicar o tipo de código. O restante do código é uma cadeia de caracteres curta para descrever a condição. Cada palavra na cadeia de caracteres é separada por um sublinhado. Por exemplo, o valor de MAPI_E_TOO_COMPLEX indica que a implementação não pôde manipular o que estava sendo solicitado na chamada. O valor de MAPI_W_PARTIAL_COMPLETION indica que a chamada foi bem-sucedida, mas que houve problemas. Somente parte da operação foi concluída com êxito.
  

