---
title: Propriedade canônica PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 945dabec4ee34d38d2474c918e779d894f4a917c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769919"
---
# <a name="pidtagrulestable-canonical-property"></a>Propriedade canônica PidTagRulesTable

  
  
**Aplica-se a**: Outlook 
  
Contém uma tabela com todas as regras aplicadas a uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RULES_TABLE  <br/> |
|Identificador:  <br/> |0x3FE1  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Regras do lado servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade está presente em todos os objetos de pasta em um servidor do Exchange que têm regras. Valores incluídos nesta propriedade são usados para ler e modificar as regras. Você pode usar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com o identificador de interface **IID_IExchangeModifyTable** para obter uma [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) interface à tabela de regras em uma pasta. Você pode usar essa interface para ler e modificar as regras. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas. 
    
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

