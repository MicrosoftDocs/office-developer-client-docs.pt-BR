---
title: Propriedade canônica PidTagSendRichInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342515"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>Propriedade canônica PidTagSendRichInfo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se o destinatário pode receber todo o conteúdo da mensagem, incluindo Rich Text Format (RTF) e objetos OLE (vinculação e incorporação de objetos). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEND_RICH_INFO  <br/> |
|Identificador:  <br/> |0x3A40  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que a lista de distribuição e os objetos do usuário de mensagens exponham essa propriedade. 
  
Essa propriedade indica se o remetente considera o destinatário como habilitado para MAPI. 
  
Quando essa propriedade é definida como TRUE, o transporte e o gateway podem transmitir o conteúdo completo da mensagem, incluindo os objetos RTF e OLE. O provedor de transporte e o gateway devem usar o formato de encapsulamento de transporte neutro (TNEF) para encapsular quaisquer propriedades que não sejam nativas para todos os sistemas de mensagens envolvidos. 
  
Quando essa propriedade é definida como FALSE, o provedor de transporte e o gateway estão livres para descartar o conteúdo da mensagem que seus clientes nativos não podem usar. Por exemplo, quando os clientes não suportam RTF, o provedor de transporte pode enviar apenas texto sem formatação. 
  
Quando essa propriedade não é definida, o comportamento padrão é determinado pela implementação do provedor de transporte, do agente de transferência de mensagens (MTA) ou do gateway. Os provedores de catálogo de endereços não são necessários para dar suporte a essa propriedade. Por exemplo, um catálogo de endereços e um provedor de transporte rigidamente acoplados podem optar por enviar TNEF, mas nunca usar RTF. 
  
O cliente não deve assumir que o provedor de transporte e o gateway usarão o TNEF em sua própria iniciativa. Alguns provedores de transporte e gateways que dão suporte a TNEF transmitem o valor dessa propriedade, mas outros recusam a construir ou enviarem TNEF se não estiverem definidos como TRUE. 
  
> [!NOTE]
> A configuração dessa propriedade e as decisões com base em seu valor, estão em uma base por destinatário. 
  
Por padrão, o MAPI define o valor como TRUE. Um cliente chamando [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) ou um provedor chamando [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) pode definir o bit **MAPI_SEND_NO_RICH_INFO** no parâmetro _PARÂMETROULFLAGS_ , que faz com que o MAPI defina essa propriedade como false. Um-offs criados pela interface do usuário usam o valor especificado pelo modelo de criação. 
  
Em chamadas para o método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) quando o nome não pode ser resolvido, mas pode ser interpretado como um endereço de Internet (SMTP), essa propriedade é definida como false. Para ser interpretado como um endereço de Internet, o nome de exibição da entrada não resolvida deve estar no formato X @ Y. Z, como "pete@pinecone.com". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> das convenções de email padrão da Internet para objetos de mensagem.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

