---
title: Seção do arquivo de configuração de formulários [verbos]
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
# <a name="form-configuration-file-verbs-section"></a>Seção do arquivo de configuração de formulários [verbos]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[verbos]** lista o conjunto completo de verbos com suporte no formulário. O formato da seção **[verbos]** é: 
  
 **Verbos**
  
 **** =  _Cadeia de caracteres_ Verb1
  
Veja a seguir um exemplo de uma seção de **[verbos]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Cada verbo é definido em um **[verbo separado.** _cadeia de caracteres_ **]** seção. Um **[verbo.** _cadeia de caracteres_ **]** descreve um único verbo oferecido pelo formulário. A entrada **DisplayName** em um **[Verb.** _cadeia de caracteres_ **]** seção especifica o nome do comando exibido na interface do usuário. A entrada de **código** corresponde ao número de verbo passado no método [IMAPIForm::D overb](imapiform-doverb.md) . A sintaxe do **verbo [.** _cadeia de caracteres_ **]** seção é: 
  
 **Verbo.** _cadeia de caracteres_ **]**
  
 **** =  _Cadeia de caracteres exibida_ DisplayName
  
 **** =  _Inteiro_ de código
  
 **** =  _Inteiro_ de sinalizadores
  
 **** Número inteiro de attrib__  =  
  
Veja a seguir um exemplo de um **verbo [.** _cadeia de caracteres_ **]** seção. 
  
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

Os verbos listados nesta seção são recuperados por um cliente usando o [método IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md). Os verbos são ativados chamando o método [IMAPIForm::D overb](imapiform-doverb.md) do formulário e passando-o número de código do verbo a ser executado. 
  

