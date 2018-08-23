---
title: Propriedade canônica PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0ea7d0a17fdb6dba047cb97290d991ce384d4750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573933"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a>Propriedade canônica PidTagInitialDetailsPane

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica a página de um modelo de exibição para exibir o primeiro.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_INITIAL_DETAILS_PANE  <br/> |
|Identificador:  <br/> |0x3F08  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tabelas de exibição MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Ele deve estar presente em todos os objetos de catálogo de endereços em um servidor de nome serviço provedor NSPI (Interface) e deve ter um valor zero (0). Não deve ser definido para qualquer objeto em um catálogo de Endereços Offline.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

