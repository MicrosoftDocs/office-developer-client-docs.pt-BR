---
title: Propriedade canônica PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415051"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Propriedade canônica PidTagReceiveFolderSettings

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma tabela de configurações de pasta de recebimento de um armazenamento de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Identificador:  <br/> |0x3415  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Armazenamento de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser excluída nas [operações IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp::CopyProps.](imapiprop-copyprops.md) Como uma propriedade do tipo PT_OBJECT, ela não pode ser recuperada com êxito pelo método [IMAPIProp::GetProps;](imapiprop-getprops.md) seu conteúdo deve ser acessado pelo [método IMAPIProp::OpenProperty,](imapiprop-openproperty.md) solicitando a interface com identificador IID_IMAPITable. Os provedores de serviços devem reportá-lo para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas, opcionalmente, pode reportá-lo ou não se ele não estiver definido. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md) Para obter mais informações, consulte [Tabelas de Pastas de Recebimento.](receive-folder-tables.md)
  
Essa propriedade contém uma tabela de mapeamentos das pastas de recebimento para o armazenamento de mensagens. Chamar **OpenProperty** nessa propriedade é equivalente a chamar **GetReceiveFolderTable** no armazenamento de mensagens. 
  
## <a name="related-resources"></a>Recursos relacionados

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

