---
title: atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408275"
---
# <a name="attdate-attributes"></a>atributos attDate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todas as propriedades MAPI relacionadas a datas e horas são mapeadas para atributos TNEF que têm o **prefixo attDate.** Todos eles são codificados como estruturas **DTR.** As datas e horas para atributos de anexo também são codificadas como estruturas **DTR.** 
  
Todas as propriedades MAPI relacionadas a datas e horas são mapeadas para atributos TNEF que têm o **prefixo attDate.** Todos eles são codificados como estruturas **DTR.** As datas e horas para atributos de anexo também são codificadas como estruturas **DTR.** 
  
Uma **estrutura DTR** é muito semelhante à estrutura **SYSTEMTIME** definida nos arquivos de título Win32. A **estrutura DTR** é codificada no fluxo TNEF como bytes **sizeof(DTR)** começando com o primeiro membro da estrutura. A **estrutura DTR** é definida no TNEF. Arquivo de header H. 
  

