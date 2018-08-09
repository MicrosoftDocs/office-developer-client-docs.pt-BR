---
title: Atributos attDate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766202"
---
# <a name="attdate-attributes"></a>Atributos attDate

  
  
**Aplica-se a**: Outlook 
  
Todas as propriedades MAPI relativos ao datas e horas são mapeadas para os atributos TNEF que possuem o prefixo **attDate** . Estas são codificadas como estruturas **DTR** . As datas e horas dos atributos do anexo são codificadas como **DTR** estruturas também. 
  
Todas as propriedades MAPI relativos ao datas e horas são mapeadas para os atributos TNEF que possuem o prefixo **attDate** . Estas são codificadas como estruturas **DTR** . As datas e horas dos atributos do anexo são codificadas como **DTR** estruturas também. 
  
Uma estrutura **DTR** é muito semelhante à estrutura **SYSTEMTIME** definida nos arquivos de cabeçalho Win32. A estrutura **DTR** é codificada no stream TNEF como bytes **sizeof(DTR)** começando com o primeiro membro da estrutura. A estrutura **DTR** é definida no TNEF. Arquivo de cabeçalho H. 
  

