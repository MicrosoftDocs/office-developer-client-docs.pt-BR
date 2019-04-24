---
title: Propriedade canônica PidTagSentRepresentingSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ed122a2-0967-4de3-a2ee-69f81ae77b16
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a9114b1c9c3f5b09c5636f7d55d7111dd86afc06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341934"
---
# <a name="pidtagsentrepresentingsmtpaddress-canonical-property"></a>Propriedade canônica PidTagSentRepresentingSmtpAddress

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o endereço de email SMTP (Simple Mail Transport Protocol) para o usuário de mensagens que é representado pelo remetente.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SENT_REPRESENTING_SMTP_ADDRESS, PR_SENT_REPRESENTING_SMTP_ADDRESS_A, PR_SENT_REPRESENTING_SMTP_ADDRESS_W  <br/> |
|Identificador:  <br/> |0x5D02  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é um exemplo das propriedades de endereço do usuário de mensagens que está sendo representado pelo remetente. Quando um aplicativo cliente envia uma mensagem em nome de outro cliente, ele deve definir todas as propriedades de remetente representadas para os valores desse cliente. Um usuário de mensagens enviando em seu próprio nome normalmente deixa as propriedades do remetente representadas como não contratadas.
  
O provedor de transporte de saída sempre deve deixar essa propriedade inalterada se tiver sido definida pelo cliente de envio. Se estiver indefinido, o provedor de transporte deve defini-la como a propriedade **PR_SENDER_SMTP_ADDRESS** ([PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)) na cópia de saída da mensagem e deixá-la desdefinida na cópia local.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar e configurar caixas de correio como delegados e interações com objetos de mensagem e calendário quando eles atuam em nome de outro usuário.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte as convenções de email padrão da Internet em objetos de mensagem.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.
    
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

