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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315418"
---
# <a name="pidlidusetnef-canonical-property"></a>Propriedade canônica PidLidUseTnef

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se o formato de encapsulamento de transporte neutro (TNEF) deve ser incluído em uma mensagem quando essa mensagem é convertida de MAPI para Multipurpose Internet Mail Extensions (MIME) ou formato SMTP (Simple Mail Transfer Protocol).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidUseTNEF  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008582  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Configuração de tempo de execução  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade especifica se o TNEF deve ser incluído em uma mensagem quando essa mensagem é convertida de TNEF para o formato MIME ou SMTP. Essa propriedade pode estar ausente e, em caso afirmativo, o TNEF não deve ser incluído na mensagem.
  
Essa propriedade só se aplica quando a mensagem é enviada de uma conta de email POP3/SMTP e não se aplica quando a mensagem é enviada por outros provedores, como o Microsoft Exchange Server.
  
Sob determinadas circunstâncias, como quando os botões de votação estão habilitados ou um objeto OLE incorporado é anexado a uma mensagem, o Outlook pode definir essa propriedade para forçar o uso de TNEF.
  
A propriedade **PR_MSG_EDITOR_FORMAT** ([PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)) pode ser usada para impor apenas o texto sem formatação e não o TNEF ao enviar uma mensagem. Como o **PidLidUseTNEF** substitui a configuração no **PR_MSG_EDITOR_FORMAT**, um aplicativo que deseja forçar o texto sem formatação em uma mensagem de saída também deve procurar por **PidLidUseTNEF** e redefini-lo como false. Além disso, o suplemento deve remover os recursos de mensagem que exigiram TNEF para evitar anexos inúteis na mensagem que foi enviada por último. 
  
Use o sinalizador **CCSF_USE_TNEF** ao chamar [IConverterSession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para converter uma mensagem MAPI de saída em um fluxo MIME também pode impor TNEF. Isso se aplica mesmo se **PidLidUseTNEF** não estiver definido. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

