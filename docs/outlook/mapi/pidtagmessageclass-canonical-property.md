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
ms.openlocfilehash: f54bdb70e9f48c89cb50e8238f8638deac8a93b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567815"
---
# <a name="pidtagmessageclass-canonical-property"></a>Propriedade canônica PidTagMessageClass

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres de texto que identifica a classe de mensagem definidas pelo remetente, como IPM. Nota. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W  <br/> |
|Identificador:  <br/> |0x001A  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Comuns  <br/> |
   
## <a name="remarks"></a>Comentários

A classe de mensagem especifica o tipo da mensagem. Determina o conjunto de propriedades definidas para a mensagem, o tipo de informações a mensagem transmite e como lidar com a mensagem. 
  
Essas propriedades contêm concatenadas com períodos de cadeias de caracteres. Cada cadeia de caracteres representa um nível de subclassificação. Por exemplo, IPM. Observação é uma subclasse de IPM e uma superclasse do IPM. Note.Private. 
  
Essas propriedades devem conter os caracteres ASCII 32 a 127 e não devem terminar com um ponto (ASCII 46). Operações de classificação e comparação devem tratá-lo como uma cadeia de caracteres diferenciam maiusculas e minúsculas. O comprimento máximo de possível é de 255 caracteres, mas, para permitir que a sala MAPI acrescentar o qualificador é recomendável que o comprimento original sejam mantidos em 128 caracteres. 
  
Cada mensagem é necessária para fornecer a essas propriedades. Normalmente, o aplicativo cliente criando uma nova mensagem define tão logo [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) retorna com êxito. Mas, se a propriedade não tiver sido definida quando o cliente chama [IMAPIProp::SaveChanges](imapiprop-savechanges.md), o armazenamento de mensagens deve defini-la como IPM. 
  
Os valores definidos pelo MAPI são: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM e CPI servem para ser apenas de superclasse, e uma mensagem deve ter pelo menos um qualificador de subclasse acrescentado antes que estão sendo armazenados ou enviados. Para obter mais informações sobre o uso de classe de mensagem, consulte [Classes de mensagens](mapi-message-classes.md). Para obter listas de propriedades obrigatórios e opcionais de classes de mensagens, consulte os subtópicos [sobre](message-properties-overview.md)propriedades de mensagem.
  
Uma classe de mensagem personalizada pode definir propriedades em um intervalo reservado para uso com essa classe de mensagem. Para obter mais informações, consulte [Sobre identificadores de propriedade](mapi-property-identifier-overview.md). 
  
Controle de classes de mensagem que recebe uma mensagem de entrada da pasta é armazenado em. Para obter mais informações, consulte o método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Para obter mais informações sobre como usar as classes de mensagem com formulários e servidores de formulário, consulte [escolhendo uma classe de mensagem](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para representar mensagens de caixa postal e fax.
    
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

