---
title: Propriedade canônica PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9dba26ab6948d7190521ff31a8732c4b058ab7c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769854"
---
# <a name="pidtagresponsibility-canonical-property"></a>Propriedade canônica PidTagResponsibility

  
  
**Aplica-se a**: Outlook 
  
Contém TRUE se algum provedor de transporte já aceita responsabilidade para entregar a mensagem para este destinatário e FALSE se o MAPI spooler considera que esse provedor de transporte deve aceitar a responsabilidade.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESPONSIBILITY  <br/> |
|Identificador:  <br/> |0x0E0F  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o MAPI spooler apresenta uma mensagem de saída para um provedor de transporte, por meio de [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), ela define essa propriedade como FALSE para todos os destinatários para os quais o MAPI spooler considera desse provedor de transporte responsável e TRUE para todos outros destinatários. O provedor de transporte deve tentar lidar com todos os destinatários com **PR_RESPONSIBILITY** definido como FALSE. Após enviar com êxito, ou definitivamente falhando enviar, para um destinatário, o provedor de transporte deve definir essa propriedade como TRUE na mensagem de origem para indicar que ela aceita a responsabilidade para que o destinatário. 
  
Se, depois de examinar um destinatário, um provedor de transporte decidir que ele não pode ou não deveria tratar, o provedor de transporte deverá manter **PR_RESPONSIBILITY** definido como FALSE. O MAPI spooler então procurará outro provedor de transporte que pode lidar com que o destinatário. O MAPI spooler basicamente criará um relatório de não entrega para quaisquer destinatários para os quais nenhum provedor de transporte aceita responsabilidade. 
  
Se o provedor de transporte tentará e falha entregar a mensagem, ele deve chamar o método [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para indicar ao MAPI os motivos para a falha, para que o MAPI pode gerar um relatório de não entrega. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

