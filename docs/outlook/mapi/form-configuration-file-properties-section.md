---
title: Seção Arquivo de Configuração do Formulário [Propriedades]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421288"
---
# <a name="form-configuration-file-properties-section"></a>Seção Arquivo de Configuração do Formulário [Propriedades]

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A **seção [Propriedades]** lista o conjunto completo de propriedades que o formulário usa e publica; ou seja, as propriedades que ele cria em suas mensagens personalizadas que os aplicativos cliente MAPI podem usar ao exibir colunas, filtrar tabelas de conteúdo, configurar pastas de resultados de pesquisa e assim por diante. Cada entrada nessa lista de propriedades faz referência a uma **[Propriedade] subsequente.** _string_ **]** section as shown following. 
  
 **[Propriedades]**
  
 **Propriedade.** _string_  =   _string_
  
O formato de uma [ **Propriedade.** _string_] seção é: 
  
 **[Propriedade.** _string_ **]**
  
 **Tipo**  =   _integer_
  
 **NmidPropset**  =   _guid_
  
 **NmidString**  =   _string_
  
 **NmidInteger**  =   _integer_
  
 **DisplayName**  =   _string_
  
 **Sinalizadores**  =   _integer_
  
 **SpecialType** = 0|1 
  
 **Enum1**  =   _string_
  
Cada **uma [propriedade.** _string_ **]** section describes a single property. A **entrada Type** especifica o tipo de propriedade MAPI, por exemplo 3 (PT_I4), da propriedade. A **entrada NmidPropset** é opcional; juntamente com a **entrada NmidString** ou **NmidInteger,** a entrada **NmidPropset** fornece o nome da propriedade. **NmidString** fornece o nome da propriedade, enquanto **NmidInteger** fornece o identificador da propriedade. **NmidString e** **NmidInteger** são mutuamente exclusivos. 
  
Se definido, **NmidPropset** deve conter o nome do conjunto de propriedades; se estiver ausente, **NmidPropset** será definido como um padrão com base na seguinte regra: se **NmidInteger** estiver presente e seu valor for menor que 0x8000, **NmidPropset** será definido como PS_MAPI. Se o valor de **NmidInteger** for definido como um inteiro maior que 0x8000 ou se estiver ausente, **NmidPropset** será definido como PS_PUBLIC_STRINGS. 
  
A **entrada DisplayName** contém o rótulo da propriedade. A **entrada SpecialType,** se presente e diferente de zero, indica que essa propriedade é uma propriedade especial. No momento, o único tipo de propriedade especial definido **é SpecialType** = 1, que indica propriedades enumeradas de cadeia de caracteres. Se **SpecialType** for definido como 1, a **entrada Enum1** referencia **o [Enum1.** _seção string_ **]** . 
  
A seguir está um exemplo de **uma seção [Properties]** e um **[Properties.** _seção string_ **]** . 
  
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

A **entrada Enum1** no exemplo de pré-referência faz referência a **uma [Enum1] subsequente.** _seção string_ **]** descrevendo uma enumeração de um tipo específico. Essa enumeração associa a primeira propriedade na **propriedade [Property.** _string_ **]** section with an integer property, called the index. Essa enumeração também contém uma lista dos valores possíveis que o par display-index pode assumir. Especificar um tipo de propriedade para a enumeração é desnecessário porque, por definição, uma entrada **Enum1** sempre tem o tipo PT_I4 especificado. O formato do **[Enum1.** _string_ **]** section is: 
  
 **[Enum1.** _string_ **]**
  
 **NmidPropset**  =   _guid_
  
 **NmidString**  =   _string_
  
 **NmidInteger**  =   _integer_
  
 **EnumCount**  =   _integer_
  
 **Val.** _inteiro_ **. Exibir cadeia de**  =   _caracteres_
  
 **Val.** _inteiro_ **. Inteiro de**  =   _índice_
  
A seguir está uma definição de propriedade de exemplo para uma propriedade enumerada chamada Risco de Incêndio com valores possíveis de Low, Medium e High.
  
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

 **[Enum1.** _string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values. Por exemplo, a classificação pode ser feita com base na ordem De baixo médio-alto em vez de ordem alta-média-baixa. 
  

