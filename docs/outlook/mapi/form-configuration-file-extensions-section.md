---
title: Seção do arquivo de configuração de formulários [extensões]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423752"
---
# <a name="form-configuration-file-extensions-section"></a>Seção do arquivo de configuração de formulários [extensões]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[Extensions]** lista os atributos estendidos do formulário, geralmente um conjunto de propriedades nomeadas, que são qualquer atributo além dos básicos listados na seção **[Description]** do arquivo de configuração de formulário. Os atributos estendidos são propriedades retornadas de **** chamadas para o método GetProps do objeto **IMAPIFormInfo** com o bit alto definido na marca da propriedade. Os aplicativos cliente podem determinar os atributos estendidos de um formulário, se houver, recuperando essas marcas. Para fazer isso, os clientes chamam o método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) , passando os nomes das propriedades do formulário e chamar o método [IMAPIProp::](imapiprop-getprops.md) GetProps para obter as propriedades. 
  
 **Das**
  
 **Extensões.** _seqüência1_ =  _seqüência2_
  
Cada seção de propriedades de extensão define um atributo de extensão usando a sintaxe da propriedade nomeada MAPI. O tipo de propriedade deve ser PT_LONG ou PT_STRING8. Não há suporte para conjuntos de propriedades que contenham cadeias de caracteres nomeadas. O formato da seção **[Extension]** é: 
  
 **Extensões.** _seqüência2_ **]**
  
 **Tipo** =  _inteiro_
  
 **** =  _GUID_ NmidPropset
  
 **NmidInteger** =  _inteiro_
  
 **Valor** =  __ |  _inteiro_ da cadeia de caracteres
  
Um exemplo de uma seção **[Extensions]** e uma seção relacionada subsequentes são mostrados a seguir. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


