---
title: Retornar Convenção de nomenclatura de valor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2c1cdd7b-82f1-46f2-a7ce-e0efe857b7cd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6786e1ca901215abd709a11401c3026d62c6ffc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279822"
---
# <a name="return-value-naming-convention"></a>Retornar Convenção de nomenclatura de valor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPICODE. O arquivo de cabeçalho H contém muitos dos valores que um cliente ou provedor de serviços pode retornar de uma implementação de método de interface ou pode ver retornados de uma chamada.
  
Os códigos para representar as condições de aviso e de falha seguem uma Convenção de nomenclatura diferente que começa com o prefixo MAPI, um sublinhado e um W ou um E para indicar o tipo de código. O restante do código é uma cadeia de caracteres curta para descrever a condição. Cada palavra da cadeia de caracteres é separada por um sublinhado. Por exemplo, o valor de erro MAPI_E_TOO_COMPLEX indica que a implementação não pôde lidar com o que estava sendo solicitado na chamada. O valor de aviso MAPI_W_PARTIAL_COMPLETION indica que a chamada foi bem-sucedida, mas que houve problemas. Somente parte da operação foi concluída com êxito.
  

