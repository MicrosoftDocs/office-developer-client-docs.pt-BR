---
title: Propriedade canônica PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332001"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Propriedade canônica PidTagAccessControlListTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma tabela que consiste em todas as listas de controle de acesso do sistema (SACL) aplicadas a uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ACL_TABLE  <br/> |
|Identificador:  <br/> |0x3FE0  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Controle de acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade está presente em todos os objetos Folder em um servidor Exchange. Os valores incluídos nessa propriedade são usados para ler e modificar listas de controle de acesso (ACLs) em pastas. Você pode usar o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) com o identificador de interface **IID_IExchangeModifyTable** para obter uma interface [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) para a tabela ACL em uma pasta. Você pode usar essa interface para ler e modificar essas ACLs. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

