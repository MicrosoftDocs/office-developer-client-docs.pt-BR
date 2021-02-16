---
title: Propriedade canônica PidTagSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEntryId
api_type:
- COM
ms.assetid: 9f311dd2-853e-46f7-966a-c2ab7a1fb6c5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0bc8b8bd76d553cc4e12e331e9fe7047ef7aaf4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358909"
---
# <a name="pidtagsenderentryid-canonical-property"></a>Propriedade canônica PidTagSenderEntryId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de entrada do remetente da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SENDER_ENTRYID  <br/> |
|Identificador:  <br/> |0x0C19  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é uma das propriedades de endereço do remetente da mensagem. Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar valores existentes anteriormente.
  
Se nenhum provedor de transporte tiver fornecido qualquer propriedade de endereço do remetente, o spooler MAPI tentará preenchê-las chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada. Se nenhum identificador de entrada tiver sido fornecido, o spooler MAPI um identificador correspondente à cadeia de caracteres "Unknown" nesta propriedade. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que representam itens RSS.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para postagem de objetos.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

