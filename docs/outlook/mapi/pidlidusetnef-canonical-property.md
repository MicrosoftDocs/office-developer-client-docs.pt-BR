---
title: Propriedade canônica PidLidUseTnef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidUseTnef
api_type:
- COM
ms.assetid: 954048d6-e2eb-43e7-b52c-c2f047bb84a4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 56f6e2355ee2e64cc766bafe27cd59454e210ab6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384974"
---
# <a name="pidlidusetnef-canonical-property"></a>Propriedade canônica PidLidUseTnef

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se o TNEF Transport Neutral Encapsulation Format () deve ser incluído em uma mensagem quando a mensagem é convertida de MAPI para o formato do Multipurpose Internet Mail Extensions (MIME) ou Simple Mail Transfer Protocol (SMTP).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidUseTNEF  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x00008582  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuração de tempo de execução  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade especifica se o TNEF deve ser incluído em uma mensagem quando a mensagem é convertida de TNEF para o formato MIME ou SMTP. Essa propriedade pode ser ausente e, em caso afirmativo, TNEF não deve ser incluído na mensagem.
  
Essa propriedade só se aplica quando a mensagem é enviada a partir de uma conta de email POP3/SMTP e não se aplica quando a mensagem é enviada por outros provedores, como o Microsoft Exchange Server.
  
Sob determinadas circunstâncias, como quando votação botões estão ativados ou uma OLE incorporado o objeto é anexado a uma mensagem, o Outlook pode definir essa propriedade para forçar o uso do TNEF.
  
A propriedade **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) pode ser usada para impor apenas texto sem formatação e não o TNEF, ao enviar uma mensagem. Porque **PidLidUseTNEF** substitui a configuração em **PR_MSG_EDITOR_FORMAT**, um aplicativo que deseja forçar o texto sem formatação em uma mensagem de saída também deve procurar **PidLidUseTNEF** e redefini-lo como FALSE. Além disso, o suplemento deve remover os recursos de mensagem que exigiam o TNEF evitar anexos não utilizável na mensagem que é enviada por último. 
  
Use o sinalizador **CCSF_USE_TNEF** ao chamar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para converter uma mensagem de MAPI de saída para um fluxo MIME também pode impor TNEF. Isso se aplica mesmo se **PidLidUseTNEF** não estiver definida. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

