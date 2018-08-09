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
ms.openlocfilehash: e93325873f1d9e89bb591d136df04aa27403375f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769770"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Propriedade canônica PidTagReceiveFolderSettings

  
  
**Aplica-se a**: Outlook 
  
Contém uma tabela de uma mensagem repositório receberão as configurações de pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Identificador:  <br/> |0x3415  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Armazenamento de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ser excluída em operações [IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações da [IMAPIProp::CopyProps](imapiprop-copyprops.md) . Como uma propriedade do tipo PT_OBJECT, ele não pode ser recuperado com êxito pelo método [IMAPIProp::GetProps](imapiprop-getprops.md) ; seu conteúdo deve ser acessado pelo método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , solicitando a interface com o identificador IID_IMAPITable. Provedores de serviços devem relatá-la para o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas pode, opcionalmente, relatá-la ou não se não estiver definida. 
  
Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . Para obter mais informações, consulte as [Tabelas de pasta de recebimento](receive-folder-tables.md).
  
Essa propriedade contém uma tabela de mapeamento das pastas de recebimento para o armazenamento de mensagens. Chamar **OpenProperty** sobre esta propriedade é equivalente a chamar **GetReceiveFolderTable** no armazenamento de mensagens. 
  
## <a name="related-resources"></a>Recursos relacionados

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

