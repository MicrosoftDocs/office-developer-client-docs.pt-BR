---
title: Seção do arquivo de configuração de formulários [Verbos]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6a06283e3eb072e1f502d0b1bd303ce9f0733578
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583971"
---
# <a name="form-configuration-file-verbs-section"></a>Seção do arquivo de configuração de formulários [Verbos]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  

