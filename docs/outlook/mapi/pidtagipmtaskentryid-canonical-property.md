---
title: Propriedade canônica PidTagIpmTaskEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmTaskEntryId
api_type:
- HeaderDef
ms.assetid: ec8b7486-b547-4a4e-96e5-1fc825b23f3d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c3845c745dcd2c18525f147308233b94fbce70d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327838"
---
# <a name="pidtagipmtaskentryid-canonical-property"></a>Propriedade canônica PidTagIpmTaskEntryId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a **EntryID** da pasta tarefas do Outlook. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_IPM_TASK_ENTRYID  <br/> |
|Identificador:  <br/> |0x36D4  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Pasta  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é lida ou gravada usando o protocolo de objeto Property e Stream. Ele é lido e gravado na caixa de entrada ou na pasta raiz. A implementação deve usar a pasta caixa de entrada quando o repositório é o do principal usuário de mensagens e deve usar a pasta raiz quando o repositório é o de um usuário delegado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar e configurar caixas de correio como delegados e interações com objetos de mensagem e calendário quando eles atuam em nome de outro usuário.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

