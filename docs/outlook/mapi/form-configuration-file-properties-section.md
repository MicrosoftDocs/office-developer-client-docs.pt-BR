---
title: Seção do arquivo de configuração de formulários [Propriedades]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f582322c8ba2ffa0369792e531adf1ec4ccb3e28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766607"
---
# <a name="form-configuration-file-properties-section"></a>Seção do arquivo de configuração de formulários [Propriedades]

  
  
**Aplica-se a**: Outlook 
  
A seção **[Propriedades]** lista o conjunto completo de propriedades que o formulário usa e publica; ou seja, as propriedades que ele cria em suas mensagens personalizadas que o cliente MAPI aplicativos podem usado ao exibir colunas, a filtragem de tabelas de conteúdo, como configurar pastas de resultados da pesquisa e assim por diante. Cada entrada na lista propriedade faz referência a um subsequentes **[propriedade.** _cadeia de caracteres_ seção de **]** conforme mostrado seguinte. 
  
 **[Propriedades]**
  
 **Propriedade.** _cadeia de caracteres_ =  _cadeia de caracteres_
  
O formato de um [ **propriedade.** _cadeia de caracteres_] seção é: 
  
 **[Propriedade.** _cadeia de caracteres_ **]**
  
 **Tipo** =  _inteiro_
  
 **NmidPropset** =  _guid_
  
 **NmidString** =  _cadeia de caracteres_
  
 **Opção NmidInteger** =  _inteiro_
  
 **DisplayName** =  _cadeia de caracteres_
  
 **Sinalizadores** =  _inteiro_
  
 **SpecialType** = 0 | 1 
  
 **Enum1** =  _cadeia de caracteres_
  
Cada **[propriedade.** _cadeia de caracteres_ seção de **]** descreve uma única propriedade. A entrada de **tipo** Especifica o tipo de propriedade MAPI, por exemplo 3 (PT_I4), da propriedade. A entrada **NmidPropset** é opcional. junto com a entrada **NmidString** ou a entrada de **opção NmidInteger** , a entrada **NmidPropset** fornece o nome da propriedade. **NmidString** fornece o nome da propriedade, enquanto a **opção NmidInteger** dá o identificador da propriedade. **NmidString** e **opção NmidInteger** são mutuamente exclusivos. 
  
Se definido, o **NmidPropset** deve conter o nome do conjunto de propriedades; Se ausente, **NmidPropset** for definido como um padrão com base em que a regra a seguir: se a **opção NmidInteger** estiver presente e seu valor for menor que 0x8000, **NmidPropset** é definido como PS_MAPI. Se o valor da **opção NmidInteger** estiver definido como um número inteiro maior 0x8000, ou se ele está ausente, **NmidPropset** é definido como PS_PUBLIC_STRINGS. 
  
A entrada de **DisplayName** contém o rótulo da propriedade. A entrada **SpecialType** , se presente, mas diferente de zero indica que esta propriedade é uma propriedade especial. No momento, o tipo de propriedade apenas especial definido é **SpecialType** = 1, que indica as propriedades de cadeia de caracteres enumerada. Se **SpecialType** estiver definida como 1, a entrada **Enum1** referencia o **[Enum1.** _cadeia de caracteres_ seção **]** . 
  
A seguir está um exemplo de uma seção **[Propriedades]** e um **[Propriedades.** _cadeia de caracteres_ seção **]** . 
  
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

A entrada **Enum1** nas referências de exemplo anterior para um subsequentes **[Enum1.** _cadeia de caracteres_ seção de **]** descrevendo uma enumeração de um determinado tipo. Uma enumeração tal associa a propriedade primeira no **[propriedade.** _cadeia de caracteres_ seção **]** com uma propriedade de inteiro, chamado o índice. Tal uma enumeração também contém uma lista dos valores possíveis que pode assumir o par de índice de exibição. Especificar um tipo de propriedade para a enumeração é desnecessário porque, por definição, uma entrada de **Enum1** sempre tem o tipo de PT_I4. O formato para o **[Enum1.** _cadeia de caracteres_ seção **]** é: 
  
 **[Enum1.** _cadeia de caracteres_ **]**
  
 **NmidPropset** =  _guid_
  
 **NmidString** =  _cadeia de caracteres_
  
 **Opção NmidInteger** =  _inteiro_
  
 **EnumCount** =  _inteiro_
  
 **Val.** _inteiro_ **. Exibição** =  _cadeia de caracteres_
  
 **Val.** _inteiro_ **. Índice** =  _inteiro_
  
A seguir está uma definição de propriedade de exemplo para uma propriedade enumerada chamada incêndio risco com os valores possíveis de baixo, médio e alto.
  
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

 **[Enum1.** _cadeia de caracteres_ seções **]** podem ser usadas por aplicativos para fins de duas: para acelerar a filtragem das propriedades usando o índice, em vez da cadeia de caracteres e classificar por diferente da ordem a ordem alfanumérica dos valores de cadeia de caracteres. Por exemplo, classificando poderia ser feita com base na ordem de baixo-médio-alto, em vez de ordem alta-Médio-baixo. 
  

