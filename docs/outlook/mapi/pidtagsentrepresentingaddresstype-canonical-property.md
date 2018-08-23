---
title: Propriedade canônica PidTagSentRepresentingAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingAddressType
api_type:
- COM
ms.assetid: 6ecbf653-1faf-47bd-81a4-20157859fdfd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 86b4b4056c86baacc63ea88d00ba81195eef762a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572274"
---
# <a name="pidtagsentrepresentingaddresstype-canonical-property"></a>Propriedade canônica PidTagSentRepresentingAddressType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tipo de endereço para o usuário de mensagens que é representado pelo remetente.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SENT_REPRESENTING_ADDRTYPE, PR_SENT_REPRESENTING_ADDRTYPE_A, PR_SENT_REPRESENTING_ADDRTYPE_W  <br/> |
|Identificador:  <br/> |0x0064  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são exemplos das propriedades de endereço para o usuário de mensagens está sendo representado pelo remetente. Quando um aplicativo cliente envia uma mensagem em nome de outro cliente, ele deve definir todas as propriedades de remetente representado para os valores para que o cliente. Um usuário de mensagens enviando em seu próprio nome geralmente deixa as propriedades de remetente representado não definidas.
  
O provedor de transporte de saída deve sempre deixar essa propriedade inalterada se ele tiver sido definido pelo cliente de envio. Se ela foi removida, o provedor de transporte deve defini-la como a propriedade **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) na cópia de saída da mensagem e deixá-lo não definidas na cópia local.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para postagem objetos.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagAddressType](pidtagaddresstype-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

