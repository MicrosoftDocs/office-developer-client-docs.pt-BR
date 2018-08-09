---
title: Propriedade canônica PidTagReceivedRepresentingEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingEntryId
api_type:
- COM
ms.assetid: 2ae2266c-f093-41e5-b4d0-e12aa0f03190
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12e4c97947cfe579f550cc6d48ca0b64750b9ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769752"
---
# <a name="pidtagreceivedrepresentingentryid-canonical-property"></a>Propriedade canônica PidTagReceivedRepresentingEntryId

  
  
**Aplica-se a**: Outlook 
  
Contém o identificador de entrada para o usuário de mensagens que é representado pelo usuário receptor.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RCVD_REPRESENTING_ENTRYID  <br/> |
|Identificador:  <br/> |0x0043  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é uma das propriedades de endereço para o usuário de mensagens que está sendo representado pelo usuário receptor. Ele deve ser definido pelo provedor de transporte de entrada, que também é responsável pela verificação do representante ou de autorização. Se nenhum usuário de mensagens estiver sendo representado, essa propriedade deverá ser definida para o identificador de entrada contido na propriedade **PR_RECEIVED_BY_ENTRYID** ([PidTagReceivedByEntryId](pidtagreceivedbyentryid-canonical-property.md)).
  
Um aplicativo cliente responder a uma mensagem recebida em nome de outro cliente deve copiar essa propriedade de mensagem recebida na propriedade **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) para a resposta.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.
    
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

