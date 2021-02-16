---
title: Seção Arquivo de Configuração do Formulário [Verbos]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417781"
---
# <a name="form-configuration-file-verbs-section"></a>Seção Arquivo de Configuração do Formulário [Verbos]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **seção [Verbos]** lista o conjunto completo de verbos suportados pelo formulário. O formato da **seção [Verbos]** é: 
  
 **[Verbos]**
  
 **Verb1**  =   _string_
  
A seguir está um exemplo de **uma seção [Verbos].** 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Cada verbo é definido em um **[Verbo] separado.** _seção string_ **]** . A **[Verbo.** _string_ **]** section describes a single verb offered by the form. A **entrada DisplayName** em um **[Verbo.** _string_ **]** section specifies the command name displayed in the user interface. A **entrada** de código corresponde ao número do verbo passado no [método IMAPIForm::D oVerb.](imapiform-doverb.md) A sintaxe do **[Verbo.** _string_ **]** section is: 
  
 **[Verbo.** _string_ **]**
  
 **DisplayName**  =   _cadeia de caracteres exibida_
  
 **Código**  =   _integer_
  
 **Sinalizadores**  =   _integer_
  
 **Atribs**  =   _integer_
  
A seguir está um exemplo de **um [Verbo.** _seção string_ **]** . 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

Os verbos listados nesta seção são recuperados por um cliente usando o [método IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md). Os verbos são ativados chamando o método [IMAPIForm::D oVerb](imapiform-doverb.md) do formulário e passando a ele o número de código do verbo a ser executado. 
  

