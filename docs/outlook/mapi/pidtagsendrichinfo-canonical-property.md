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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386436"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>Propriedade canônica PidTagSendRichInfo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se o destinatário poderá receber todo o conteúdo de mensagem, incluindo formato Rich Text (RTF) e objetos de vinculação e incorporação de objetos (OLE). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEND_RICH_INFO  <br/> |
|Identificador:  <br/> |0x3A40  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que a lista de distribuição e objetos de usuário de mensagens exponham essa propriedade. 
  
Esta propriedade indica se o remetente considera o destinatário a ser habilitado a MAPI. 
  
Quando essa propriedade é definida como TRUE, o transporte e o gateway podem transmitir todo o conteúdo da mensagem, incluindo os objetos OLE e RTF. O provedor de transporte e o gateway devem usar o TNEF Transport Neutral Encapsulation Format () para encapsular todas as propriedades que não são nativas todos os sistemas mensagens envolvidos. 
  
Quando essa propriedade é definida como FALSE, o provedor de transporte e o gateway são livres para descartar o conteúdo da mensagem que não é possível usar a seus clientes nativos. Por exemplo, quando os clientes não suportam RTF, o provedor de transporte que pode enviar apenas texto sem formatação. 
  
Quando essa propriedade não estiver definida, o comportamento padrão é determinado pela implementação do provedor de transporte, o agente de transferência de mensagem (MTA) ou gateway. Provedores de catálogo de endereços não são necessárias para dar suporte a essa propriedade. Por exemplo, um provedor de transporte e o catálogo de endereços ligação estreita pode optar por enviar TNEF, mas nunca usar o formato RTF. 
  
O cliente não deve supor que o provedor de transporte e o gateway usará o TNEF em sua própria iniciativa. Alguns provedores de transporte e gateways que oferecem suporte TNEF transmitem sem relação com o valor dessa propriedade, mas outros recusar construir ou enviar o TNEF se ele não estiver definido como TRUE. 
  
> [!NOTE]
> A configuração desta propriedade, e as decisões com base em seu valor, estão em uma base por destinatário. 
  
Por padrão, o MAPI define o valor como TRUE. Um cliente chamar [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) ou um provedor chamar [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) pode definir o bit **MAPI_SEND_NO_RICH_INFO** no parâmetro _ulFlags_ , que faz com que o MAPI definir essa propriedade como FALSE. Algo isolado criados pela interface do usuário use o valor especificado pelo modelo de criação. 
  
Em chamadas para o método [IAddrBook::ResolveName](iaddrbook-resolvename.md) quando o nome não pode ser resolvido, mas pode ser interpretado como um endereço de Internet (SMTP), essa propriedade é definida como FALSE. Para ser interpretado como um endereço de Internet, o nome para exibição da entrada de não-resolvida deve estar no formato X@Y. Z, como "pete@pinecone.com". 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> os objetos de convenções de email padrão da Internet para a mensagem.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

