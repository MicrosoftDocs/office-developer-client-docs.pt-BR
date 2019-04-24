---
title: Propriedade canônica PidTagMemberId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberId
api_type:
- HeaderDef
ms.assetid: 64faef3c-27b2-49d2-9d0c-8b9d33f1cb71
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b5d1d4456856f1640bbed8589fc0583060cd2520
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342634"
---
# <a name="pidtagmemberid-canonical-property"></a>Propriedade canônica PidTagMemberId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de um membro da tabela que tem os direitos descritos em uma pasta ou caixa de correio do Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MEMBER_ID  <br/> |
|Identificador:  <br/> |0x6671  <br/> |
|Tipo de dados:  <br/> |PT_I8  <br/> |
|Área:  <br/> |Controle de acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade retorna um identificador exclusivo para a tabela. Um identificador de usuário de diretório é associado a cada identificador de membro e é fornecido por essa propriedade. Essa propriedade é usada pela interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) para recuperar o identificador de entrada de diretório de um membro com direitos explícitos em uma pasta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Lida com a recuperação de listas de permissões de pastas armazenadas no servidor.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

