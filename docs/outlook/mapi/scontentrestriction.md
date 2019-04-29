---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423661"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de conteúdo, que é usada para limitar um modo de exibição de tabela apenas às linhas que incluem uma coluna com conteúdo correspondente a uma cadeia de caracteres de pesquisa. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>Members

**ulFuzzyLevel**
  
> Configurações de opção que definem o nível de precisão que a restrição de conteúdo deve impor quando você verifica se há uma correspondência.
    
   Os **16 bits inferiores** do membro **ulFuzzyLevel** se aplicam às propriedades do tipo PT_BINARY e PT_STRING8 e devem ser definidos como um dos seguintes valores: 
    
   - FL_FULLSTRING: para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida na propriedade identificada por **ulPropTag**.
        
   - FL_PREFIX: para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve aparecer no início da propriedade identificada por **ulPropTag**. As duas cadeias de caracteres devem ser comparadas apenas com o comprimento da cadeia de caracteres de pesquisa indicada por **lpProp**. 
        
   - FL_SUBSTRING: para corresponder, a cadeia de caracteres de pesquisa **lpProp** deve estar contida em qualquer lugar na propriedade identificada por **ulPropTag**. 
        
   Os **16 bits superiores** do membro **ulFuzzyLevel** se aplicam apenas às propriedades do tipo PT_STRING8 e podem ser definidos com os seguintes valores em qualquer combinação: 
        
   - FL_IGNORECASE: a comparação deve ser feita sem considerar o uso de maiúsculas e minúsculas. 
        
   - FL_IGNORENONSPACE: a comparação deve ignorar caracteres de espaçamento não definidos por Unicode, como marcas diacríticos. 
        
   - FL_LOOSE: a comparação deve fornecer uma correspondência sempre que possível, ignorando os caracteres de maiúsculas e minúsculas. 
    
**ulPropTag**
  
> Marca de propriedade que identifica a propriedade de cadeia de caracteres a ser verificada quanto à sequência de pesquisa. 
    
**lpProp**
  
> Ponteiro para uma estrutura de valor de propriedade que contém o valor da cadeia de caracteres a ser usado como a sequência de pesquisa.
    
## <a name="remarks"></a>Comentários

Há duas marcas de propriedade em uma estrutura **SContentRestriction** : uma no membro **ulPropTag** e a outra no membro **ulPropTag** da estrutura **SPropValue** apontada por **lpProp**. Em ambas as marcas, MAPI requer apenas o campo tipo de propriedade e ignora o campo identificador de propriedade. No enTanto, os dois tipos de propriedade devem coincidir, ou o valor de erro MAPI_E_TOO_COMPLEX é retornado quando a restrição é usada em uma chamada para imApitable [:: Restrict](imapitable-restrict.md) ou IMAPITable [:: FindRow](imapitable-findrow.md). 
  
Os valores FL_FULLSTRING, FL_PREFIX e FL_SUBSTRING são mutuamente exclusivos. Apenas uma delas pode ser definida, e uma delas deve ser definida. Seus significados são fixos e o provedor deve implementá-los exatamente como definido. O provedor deve retornar MAPI_E_TOO_COMPLEX se não puder suportar esses valores. 
  
Os valores FL_IGNORECASE, FL_IGNORENONSPACE e FL_LOOSE são independentes. Qualquer lugar de zero para todos os três podem ser definidos. Suas definições são fornecidas apenas como uma orientação e o provedor é livre para implementar seu significado específico de cada sinalizador. O provedor não deve retornar nenhuma indicação de erro se não tiver nenhuma implementação de um sinalizador especificado. 
  
O resultado de uma restrição de conteúdo imposta a uma propriedade é indefinido quando a propriedade não existe. Quando um cliente requer um comportamento bem definido para tal restrição e não tem certeza se a propriedade existe por exemplo, ela não é uma coluna obrigatória de uma tabela que deve criar uma restrição **e** para ingressar na restrição de conteúdo com uma restrição existir. Use uma estrutura [SExistRestriction](sexistrestriction.md) para definir a restrição existir e uma estrutura [SAndRestriction](sandrestriction.md) para definir a restrição **e** . 
  
Para obter mais informações sobre a estrutura e as restrições do **SContentRestriction** em geral, consulte [about Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Confira também

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Estruturas MAPI](mapi-structures.md)

