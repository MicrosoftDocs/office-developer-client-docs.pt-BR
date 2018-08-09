---
title: Seção do arquivo de configuração de formulários [Extensões]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7c26b86ad4d6c7fd565abddbfc76f50ac3dccaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766572"
---
# <a name="form-configuration-file-extensions-section"></a>Seção do arquivo de configuração de formulários [Extensões]

  
  
**Aplica-se a**: Outlook 
  
A seção **[Extensions]** lista os atributos estendidos do formulário, geralmente um conjunto nomeado de propriedade, que são atributos além dos básicos listados na seção **[descrição]** do arquivo de configuração de formulário. Os atributos estendidos são retornadas de chamadas para o método **GetProps** do objeto **IMAPIFormInfo** com alto definido o bit definido na marca de propriedade de propriedades. Aplicativos cliente podem determinar os atributos estendidos de um formulário, se houver, recuperando essas marcas. Para fazer isso, os clientes chamar o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , passando nos nomes de propriedades do formulário e chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) para obter as propriedades. 
  
 **[Extensions]**
  
 **Extensão.** _sequência1_ =  _sequência2_
  
Cada seção de propriedade de extensão define um atributo de extensão usando MAPI denominada a sintaxe da propriedade. O tipo de propriedade deve ser PT_LONG ou PT_STRING8. Conjuntos de propriedades que contém as cadeias de caracteres nomeadas não são suportados. O formato da seção **[extensão]** é: 
  
 **[Extensão.** _Sequência2_ **]**
  
 **Tipo** =  _inteiro_
  
 **NmidPropset** =  _guid_
  
 **Opção NmidInteger** =  _inteiro_
  
 **Valor** =  _cadeia de caracteres_ |  _inteiro_
  
Um exemplo de uma seção **[Extensions]** e uma seção relacionada subsequente é mostrado a seguir. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


