---
title: Seção do arquivo de configuração de formulários [Propriedades]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328102"
---
# <a name="form-configuration-file-properties-section"></a>Seção do arquivo de configuração de formulários [Propriedades]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A seção **[Propriedades]** lista o conjunto completo de propriedades que o formulário usa e publica; ou seja, as propriedades que ele cria em suas mensagens personalizadas que os aplicativos cliente MAPI podem usar ao exibir colunas, filtrar tabelas de conteúdo, configurar pastas de resultados de pesquisa e assim por diante. Cada entrada nessa lista de propriedades faz referência a uma subseqüente **[Property.** _cadeia de caracteres_ **]** como mostrado a seguir. 
  
 **Propriedades**
  
 **Propriedades.** __ cadeia de caracteres String__  =  
  
O formato de uma **Propriedade [.** _cadeia de caracteres_] seção é: 
  
 **Propriedades.** _cadeia de caracteres_ **]**
  
 **Tipo** =  _inteiro_
  
 **** =  _GUID_ NmidPropset
  
 **** =  _Cadeia de caracteres_ NmidString
  
 **NmidInteger** =  _inteiro_
  
 **** =  _Cadeia de caracteres_ DisplayName
  
 **** =  _Inteiro_ de sinalizadores
  
 **Specialtype** = 0 | 1 
  
 **** =  _Cadeia de caracteres_ Enum1
  
Cada **[propriedade.** _cadeia de caracteres_ **]** descreve uma única propriedade. A entrada **Type** especifica o tipo de propriedade MAPI, por exemplo 3 (PT_I4), da propriedade. A entrada **NmidPropset** é opcional; juntamente com a entrada **NmidString** ou a entrada **NmidInteger** , a entrada **NmidPropset** fornece o nome da propriedade. **NmidString** fornece o nome da propriedade, enquanto **NmidInteger** fornece o identificador da propriedade. **NmidString** e **NmidInteger** são mutuamente exclusivos. 
  
Se definido, **NmidPropset** deve conter o nome do conjunto de propriedades; Se estiver ausente, **NmidPropset** é definido como um padrão baseado na seguinte regra: se **NmidInteger** estiver presente e seu valor for menor que 0x8000, **NmidPropset** será definido como PS_MAPI. Se o valor de **NmidInteger** for definido como um inteiro maior que 0x8000, ou se estiver ausente, **NmidPropset** é definido como PS_PUBLIC_STRINGS. 
  
A entrada **DisplayName** contém o rótulo da propriedade. A **** entrada specialtype, se presente e diferente de zero indica que essa propriedade é uma propriedade especial. No momento, o único tipo de propriedade especial definido **** é specialtype = 1, que indica as propriedades enumeradas da cadeia de caracteres. Se **specialtype** for definido como 1, a entrada **Enum1** referenciará **[Enum1.** _cadeia de caracteres_ **]** seção. 
  
Veja a seguir um exemplo de uma seção **[properties]** e de **[Properties.** _cadeia de caracteres_ **]** seção. 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

A entrada **Enum1** no exemplo anterior faz referência a um **[Enum1.** _cadeia de caracteres_ **]** seção descrevendo uma enumeração de um tipo específico. Tal enumeração associa a primeira propriedade na **Propriedade [.** _cadeia de caracteres_ **]** com uma propriedade de número inteiro, chamada de índice. Tal enumeração também contém uma lista dos possíveis valores que o par de índice de exibição pode assumir. A especificação de um tipo de propriedade para a enumeração é desnecessária porque por definição uma entrada **Enum1** sempre tem o tipo PT_I4. O formato para o **[Enum1.** _cadeia de caracteres_ **]** seção é: 
  
 **[Enum1.** _cadeia de caracteres_ **]**
  
 **** =  _GUID_ NmidPropset
  
 **** =  _Cadeia de caracteres_ NmidString
  
 **NmidInteger** =  _inteiro_
  
 **EnumCount** =  _inteiro_
  
 **Val.** _número inteiro_ **. ** =  _Cadeia de caracteres_ de exibição
  
 **Val.** _número inteiro_ **. ** =  _Inteiro_ de índice
  
A seguir está um exemplo de definição de propriedade para uma propriedade enumerada chamada de risco de incêndio com valores possíveis de baixo, médio e alto.
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 **[Enum1.** _cadeia de caracteres_ **]** as seções podem ser usadas por aplicativos para duas finalidades: acelerar a filtragem de propriedades usando o índice em vez da cadeia de caracteres e classificar por uma ordem diferente da ordem alfanumérica dos valores de cadeia de caracteres. Por exemplo, a classificação pode ser feita com base na ordem baixa-média-alta em vez da ordem alta-média-baixa. 
  

