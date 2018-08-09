---
title: Propriedade canônica PidTagExchangeProfileSectionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 37a318df01101487fe0e8970251201c2515d1e8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769214"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Propriedade canônica PidTagExchangeProfileSectionId

  
  
**Aplica-se a**: Outlook 
  
Contém um GUID gerado dinamicamente usado para determinar uma conta quando você estiver usando várias contas do Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Identificador:  <br/> |0x3d150102  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Várias contas do Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam várias contas do Exchange, em vez de uma única conta do Exchange. Para acomodar várias contas do Exchange, o layout do perfil MAPI foi alterado. No Microsoft Office Outlook 2007 e versões anteriores, perfis contidos uma seção de perfil fixa dedicada para configurações do Exchange, como o nome do servidor, nome de usuário e o arquivo de pasta Offline (. ost). local. Essas configurações foram identificadas usando um identificador exclusivo, a propriedade **pbGlobalProfileSectionGuid** . A seção usada para configurações do Exchange é chamada a seção de perfil Global do Exchange. Para obter mais informações sobre o perfil Global do Exchange no Outlook 2007, consulte [como abrir a seção de perfil Global](http://support.microsoft.com/kb/188482).
  
Um local de seção perfil fixo não mais é suficiente para acomodar várias contas do Exchange. Em vez disso, para cada conta do Exchange no seu perfil, existe uma seção dedicada ao configurações dessa conta. Nova seção usada para configurações do Exchange é identificada pelo identificador exclusivo **emsmdbUID**.
  
A seção de perfil de serviço de mensagem para a conta do Exchange, você encontrará uma propriedade que contenha um GUID que seja gerado dinamicamente no momento em que a conta é criada. Este GUID é armazenado na propriedade **PidTagExchangeProfileSectionId** . Repositórios de mensagem e contêineres do catálogo de endereços expõem uma propriedade para determinar qual eles pertencem a conta do Exchange. Acessível na tabela de serviços de mensagem, cada serviço Exchange expõe essa propriedade. 
  
É possível recuperar essa propriedade por meio de uma chamada para [IMAPIProp::GetProps](imapiprop-getprops.md) em **PidTagExchangeProfileSectionId** após consultando para qualquer uma das seguintes interfaces: 
  
- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Se o objeto não é associado com o Exchange, a chamada retorna **E_NOT_FOUND**.
  
Você pode restringir contêineres em um **PidTagExchangeProfileSectionId** ao exibir o catálogo de endereços. Depois que você tiver um contêiner aberto, você pode consultar **emsmdbUID** a partir dele. Também é importante observar que se um destinatário foi selecionado de um catálogo de endereços do Exchange, o destinatário também tiver a **PidTagExchangeProfileSectionId** em sua lista de propriedades. 
  
> [!NOTE]
> Em toda as amostras de código e cabeçalhos de função, este GUID é conhecido como **emsmdbUID**. 
  
Uma das contas Exchange está marcada como conta legada do Exchange. Geralmente, é a primeira conta adicionada ao perfil. Todas as chamadas para abrir **pbGlobalProfileSectionGuid** é redirecionada para a seção global do Exchange da conta de legado. As chamadas de modelo de objeto que interagem com a conta do Exchange não-herdada também interagem com a conta legada do Exchange. 
  
O serviço Exchange herdado tem a propriedade **PR_EMSMDB_LEGACY** (0x3D18000B), que é definido como **true** na tabela de serviços de mensagem. 
  
O herdado **emsmdbUID** também é marcada na Global seção perfil do Outlook do perfil como **PidTagExchangeProfileSectionId**. Código escrito para dar suporte a várias contas do Exchange não deve ter que recuperar o herdado **emsmdbUID** porque ele deve obter o correto **emsmdbUID**, dependendo da conta em com que seu código está interagindo.
  
## <a name="see-also"></a>Confira também



[Usar várias contas do Exchange](using-multiple-exchange-accounts.md)


[Como abrir a seção perfil Global](http://support.microsoft.com/kb/188482)

