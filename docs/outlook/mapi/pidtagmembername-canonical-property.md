---
title: Propriedade canônica PidTagMemberName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberName
api_type:
- HeaderDef
ms.assetid: e19129bf-d07c-4d2e-9d4d-edbfda088ea7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a119cf1446600153e433c4aae99037d9810015c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342480"
---
# <a name="pidtagmembername-canonical-property"></a>Propriedade canônica PidTagMemberName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de exibição de um membro da tabela ACL (lista de controle de acesso).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MEMBER_NAME, PR_MEMBER_NAME_A, PR_MEMBER_NAME_W  <br/> |
|Identificador:  <br/> |0x6672  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Controle de Acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são usadas pela interface [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) para exibir o nome de um membro de uma tabela ACL, que é uma pessoa ou função com direitos explícitos em uma pasta ou caixa de correio. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Lida com a recuperação de listas de permissões de pasta armazenadas no servidor.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

