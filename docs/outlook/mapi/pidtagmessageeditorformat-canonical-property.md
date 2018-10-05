---
title: Propriedade canônica PidTagMessageEditorFormat
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401570"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Propriedade canônica PidTagMessageEditorFormat

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o formato para um editor a ser usado para exibir uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Identificador:  <br/> |0x5909  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores possíveis para **PR_MSG_EDITOR_FORMAT** podem ser uma destas opções: 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |O formato para usar o editor é desconhecido.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |O editor deve exibir a mensagem no formato de texto sem formatação.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |O editor deve exibir a mensagem no formato HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |O editor deve exibir a mensagem em formato Rich Text.  <br/> |
   
Por padrão, email mensagens (com a classe de mensagem **IPM. Observação** ou com uma classe de mensagem personalizada derivada de **IPM. Observe**) enviadas a partir de um email POP3/SMTP conta são enviadas no TNEF Transport Neutral Encapsulation Format (). A propriedade **PR_MSG_EDITOR_FORMAT** pode ser usada para impor apenas texto sem formatação e não o TNEF, ao enviar uma mensagem. Se **PR_MSG_EDITOR_FORMAT** for definido como **EDITOR_FORMAT_PLAINTEXT**, a mensagem é enviada como texto sem formatação sem TNEF. Se **PR_MSG_EDITOR_FORMAT** for definido como **EDITOR_FORMAT_RTF**, a codificação TNEF implicitamente está habilitada e a mensagem é enviada usando o formato de Internet padrão especificado no cliente do Outlook.
  
Existem dois outros meios para impor o uso de TNEF ao enviar uma mensagem.
  
- A definição de **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) denominado propriedade como True em uma mensagem indica o que TNEF deve ser incluído ao converter a mensagem MAPI para MIME/SMTP. Observe que **dispidUseTNEF** só se aplica quando a mensagem é enviada a partir de uma conta de email POP3/SMTP e não se aplica quando a mensagem é enviada por outros provedores, como o Microsoft Exchange Server. **dispidUseTNEF** sobrescreve a configuração no **PR_MSG_EDITOR_FORMAT**.
    
- Usar o sinalizador **CCSF_USE_TNEF** ao chamar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para converter uma mensagem de saída de MAPI em um fluxo MIME também pode impor o TNEF. Isso se aplica mesmo se **dispidUseTNEF** não estiver definida. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicos que são usadas em operações remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

