---
title: Seção de [verbos] do arquivo de configuração de formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766589"
---
# <a name="form-configuration-file-verbs-section"></a>Seção de [verbos] do arquivo de configuração de formulário

  
  
**Aplica-se a**: Outlook 
  
Seção **[verbos]** lista o conjunto completo de verbos suportados pelo formulário. O formato da seção **[verbos]** é: 
  
 **[Verbos]**
  
 **Verb1** =  _cadeia de caracteres_
  
A seguir está um exemplo de uma seção **[verbos]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Cada verbo é definido em um separado **[verbo.** _cadeia de caracteres_ seção **]** . Uma **[verbo.** _cadeia de caracteres_ **]** seção descreve um único verbo oferecido pelo formulário. A entrada de **DisplayName** em um **[verbo.** _cadeia de caracteres_ seção **]** Especifica o nome do comando exibido na interface do usuário. A entrada de **código** corresponde ao número verbo passado no método [IMAPIForm::DoVerb](imapiform-doverb.md) . A sintaxe para o **[verbo.** _cadeia de caracteres_ seção **]** é: 
  
 **[Verbo.** _cadeia de caracteres_ **]**
  
 **DisplayName** =  _exibido a cadeia de caracteres_
  
 **Código** =  _inteiro_
  
 **Sinalizadores** =  _inteiro_
  
 **Atributos** =  _inteiro_
  
A seguir está um exemplo de uma **[verbo.** _cadeia de caracteres_ seção **]** . 
  
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

Verbos listados nesta seção são recuperados por um cliente usando o [método IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md). Verbos serão ativados chamando o método de [IMAPIForm::DoVerb](imapiform-doverb.md) do formulário e passando-lhe o número de código do verbo a ser executada. 
  

