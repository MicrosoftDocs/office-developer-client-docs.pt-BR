---
title: Atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567010"
---
# <a name="attdate-attributes"></a>Atributos attDate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todas as propriedades MAPI relativos ao datas e horas são mapeadas para os atributos TNEF que possuem o prefixo **attDate** . Estas são codificadas como estruturas **DTR** . As datas e horas dos atributos do anexo são codificadas como **DTR** estruturas também. 
  
Todas as propriedades MAPI relativos ao datas e horas são mapeadas para os atributos TNEF que possuem o prefixo **attDate** . Estas são codificadas como estruturas **DTR** . As datas e horas dos atributos do anexo são codificadas como **DTR** estruturas também. 
  
Uma estrutura **DTR** é muito semelhante à estrutura **SYSTEMTIME** definida nos arquivos de cabeçalho Win32. A estrutura **DTR** é codificada no stream TNEF como bytes **sizeof(DTR)** começando com o primeiro membro da estrutura. A estrutura **DTR** é definida no TNEF. Arquivo de cabeçalho H. 
  

