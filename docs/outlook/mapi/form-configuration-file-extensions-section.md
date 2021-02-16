---
title: Seção Arquivo de Configuração de Formulário [Extensões]
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
# <a name="form-configuration-file-extensions-section"></a>Seção Arquivo de Configuração de Formulário [Extensões]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[Extensões]** lista os atributos estendidos do formulário, normalmente um conjunto de propriedades nomeados, que são quaisquer atributos além dos básicos listados na seção **[Descrição]** do arquivo de configuração do formulário. Atributos estendidos são propriedades retornadas de chamadas para o método **GetProps** do objeto **IMAPIFormInfo** com o bit alto definido na marca de propriedade. Os aplicativos cliente podem determinar os atributos estendidos de um formulário, se necessário, recuperando essas marcas. Para fazer isso, os clientes chamam o método [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) passando os nomes das propriedades do formulário e chamam o método [IMAPIProp::GetProps](imapiprop-getprops.md) para obter as propriedades. 
  
 **[Extensões]**
  
 **Extensão.** _string1_  =   _string2_
  
Cada seção de propriedade de extensão define um atributo de extensão usando a sintaxe de propriedade nomeada MAPI. O tipo de propriedade deve ser PT_LONG ou PT_STRING8. Não há suporte para conjuntos de propriedades que contenham cadeias de caracteres nomeadas. O formato da **seção [Extensão]** é: 
  
 **[Extensão.** _string2_ **]**
  
 **Tipo**  =   _integer_
  
 **NmidPropset**  =   _guid_
  
 **NmidInteger**  =   _integer_
  
 **Valor**  =   _string_  |   _integer_
  
Um exemplo de uma **seção [Extensões]** e uma seção relacionada subsequente é mostrado a seguir. 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


