---
title: Propriedade canônica PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359259"
---
# <a name="pidtagmessageclass-canonical-property"></a>Propriedade canônica PidTagMessageClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres de texto que identifica a classe de mensagem definida pelo remetente, como IPM. Observação. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Identificador:  <br/> |0x001A  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Comum  <br/> |
   
## <a name="remarks"></a>Comentários

A classe de mensagem Especifica o tipo da mensagem. Ele determina o conjunto de propriedades definido para a mensagem, o tipo de informação que a mensagem transmite e como lidar com a mensagem. 
  
Essas propriedades contêm cadeias de caracteres concatenadas com pontos. Cada cadeia de caracteres representa um nível de subclassificação. Por exemplo, IPM. Observe que é uma subclasse de IPM e uma superclasse de IPM. Note. Private. 
  
Essas propriedades devem consistir nos caracteres ASCII 32 a 127 e não devem terminar com um ponto (ASCII 46). As operações de classificação e comparação devem tratá-lo como uma cadeia de caracteres que não diferencia maiúsculas de minúsculas. O tamanho máximo possível é de 255 caracteres, mas para permitir que a sala de MAPI Anexe os qualificadores, é recomendável que o comprimento original seja mantido abaixo de 128 caracteres. 
  
Todas as mensagens são necessárias para fornecer essas propriedades. Normalmente, o aplicativo cliente que cria uma nova mensagem a define assim que [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) é retornado com êxito. Mas, se a propriedade não tiver sido definida quando o cliente chama [IMAPIProp:: SaveChanges](imapiprop-savechanges.md), o repositório de mensagens deverá defini-la como IPM. 
  
Os valores definidos por MAPI são: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM e IPC se destinam apenas a superclasses e uma mensagem deve ter pelo menos um qualificador de subclasse acrescentado antes de ser armazenado ou enviado. Para obter mais informações sobre o uso da classe de mensagem, consulte [Message classes](mapi-message-classes.md). Para obter listas de propriedades obrigatórias e opcionais para classes de mensagens, consulte os subtópicos [sobre propriedades de mensagem](message-properties-overview.md).
  
Uma classe de mensagem personalizada pode definir propriedades em um intervalo reservado para uso somente com essa classe de mensagem. Para obter mais informações, consulte [about Property Identifiers](mapi-property-identifier-overview.md). 
  
Classes de mensagens controle em qual pasta de recebimento uma mensagem de entrada é armazenada. Para obter mais informações, consulte o método [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Para obter mais informações sobre como usar classes de mensagem com formulários e servidores de formulário, consulte [escolhendo uma classe de mensagem](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para representar a caixa postal e mensagens de fax.
    
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

