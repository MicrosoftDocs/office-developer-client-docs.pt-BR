---
title: Expandir listas de distribuição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5731a35b5d570669d8606be6dd6ca1a23fb87e88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414134"
---
# <a name="expanding-distribution-lists"></a>Expandir listas de distribuição

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para solicitar que o MAPI expanda uma lista de distribuição**
  
- Defina sua propriedade **PR_ADDRTYPE** ([PIDTAGADDRESSTYPE](pidtagaddresstype-canonical-property.md)) como MAPIPDL.
    
    MAPI expande endereços com esse tipo antes de enviar a mensagem para o provedor de transporte.
    

