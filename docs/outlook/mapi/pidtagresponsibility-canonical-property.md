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
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330118"
---
# <a name="pidtagresponsibility-canonical-property"></a>Propriedade canônica PidTagResponsibility

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se algum provedor de transporte já aceitou a responsabilidade de entregar a mensagem a esse destinatário e FALSE se o spooler MAPI considera que esse provedor de transporte deve aceitar responsabilidade.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESPONSIBILITY  <br/> |
|Identificador:  <br/> |0x0E0F  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI não-transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o spooler MAPI apresenta uma mensagem de saída para um provedor de transporte, por meio de [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), ele define essa propriedade como false para todos os destinatários para os quais o spooler MAPI considera o provedor de transporte responsável e true para todos os outros destinatários. O provedor de transporte deve tentar lidar com todos os destinatários com **PR_RESPONSIBILITY** definido como false. Após o envio bem-sucedido, ou sem falhas, o envio, para um destinatário, o provedor de transporte deve definir essa propriedade como TRUE na mensagem de origem para indicar que ela aceitou a responsabilidade por esse destinatário. 
  
Se, após examinar um destinatário, um provedor de transporte decidir que ele não pode ou não deve tratá-lo, o provedor de transporte deve deixar **PR_RESPONSIBILITY** definido como false. O spooler MAPI procurará por outro provedor de transporte que possa lidar com esse destinatário. O spooler MAPI cria, por fim, um relatório de não entrega para os destinatários para os quais nenhum provedor de transporte aceita responsabilidade. 
  
Se o provedor de transporte tentar entregar a mensagem, ele deverá chamar o método [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para indicar a MAPI dos motivos da falha, para que o MAPI possa gerar um relatório de não entrega. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

