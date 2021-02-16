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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325631"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a>Propriedade canônica PidTagMessageEditorFormat

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o formato de um editor a ser usado para exibir uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MSG_EDITOR_FORMAT  <br/> |
|Identificador:  <br/> |0x5909  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Os valores possíveis **para PR_MSG_EDITOR_FORMAT** podem ser um dos seguintes: 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|**EDITOR_FORMAT_DONTKNOW** <br/> |O formato para o editor usar é desconhecido.  <br/> |
|**EDITOR_FORMAT_PLAINTEXT** <br/> |O editor deve exibir a mensagem no formato de texto sem formatação.  <br/> |
|**EDITOR_FORMAT_HTML** <br/> |O editor deve exibir a mensagem no formato HTML.  <br/> |
|**EDITOR_FORMAT_RTF** <br/> |O editor deve exibir a mensagem no formato Rich Text.  <br/> |
   
Por padrão, mensagens de email (com o IPM de classe de **mensagem. Observe** ou com uma classe de mensagem personalizada derivada do **IPM. Observação**) enviadas de uma conta de email POP3/SMTP são enviadas no TNEF (Transport Neutral Encapsulation Format). A **PR_MSG_EDITOR_FORMAT** propriedade pode ser usada para impor somente texto sem texto sem texto, e não TNEF, ao enviar uma mensagem. Se **PR_MSG_EDITOR_FORMAT** for definido como **EDITOR_FORMAT_PLAINTEXT**, a mensagem será enviada como texto sem TNEF. Se **PR_MSG_EDITOR_FORMAT** for definida como EDITOR_FORMAT_RTF , **a** codificação TNEF será habilitada implicitamente e a mensagem será enviada usando o formato padrão da Internet especificado no cliente do Outlook.
  
Há duas outras maneiras de impor o uso de TNEF ao enviar uma mensagem.
  
- Definir a propriedade nomeada **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) como True em uma mensagem indica que o TNEF deve ser incluído ao converter a mensagem de MAPI para MIME/SMTP. Observe que **dispidUseTNEF** só se aplica quando a mensagem é enviada de uma conta de email POP3/SMTP e não se aplica quando a mensagem é enviada por outros provedores, como o Microsoft Exchange Server. **dispidUseTNEF** substitui a configuração em **PR_MSG_EDITOR_FORMAT**.
    
- Usar o **sinalizador CCSF_USE_TNEF** ao chamar [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) para converter uma mensagem MAPI de saída em um fluxo MIME também pode impor o TNEF. Isso se aplica mesmo se **dispidUseTNEF** não estiver definido. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define as estruturas de dados básicas que são usadas em operações remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

