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
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316426"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Propriedade canônica PidTagExchangeProfileSectionId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um GUID gerado dinamicamente usado para determinar uma conta quando você estiver usando várias contas do Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Identificador:  <br/> |0x3d150102  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Várias contas do Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

O Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam várias contas do Exchange em vez de uma única conta do Exchange. Para acomodar várias contas do Exchange, o layout de perfil MAPI foi alterado. No Microsoft Office Outlook 2007 e versões anteriores, os perfis continham uma seção de perfil fixa dedicada às configurações do Exchange, como nome do servidor, nome de usuário e arquivo de Pasta Offline (.ost). local. Essas configurações foram identificadas usando um identificador exclusivo, a **propriedade pbGlobalProfileSectionGuid.** A seção usada para as configurações do Exchange é chamada de Seção de Perfil Global do Exchange. 
  
Um local de seção de perfil fixo não é mais suficiente para acomodar várias contas do Exchange. Em vez disso, para cada conta do Exchange em seu perfil, existe uma seção dedicada às configurações dessa conta. A nova seção usada para as configurações do Exchange é identificada pelo identificador exclusivo **emsmdbUID**.
  
Na seção de perfil de serviço de mensagens para a conta do Exchange, você pode encontrar uma propriedade que contém um GUID que é gerado dinamicamente no momento em que a conta é criada. Esse GUID é armazenado na propriedade **PidTagExchangeProfileSectionId.** Os armazenamentos de mensagens e os contêineres do livro de endereços expõem uma propriedade para determinar a qual conta do Exchange pertencem. Acessível na tabela de serviços de mensagens, cada serviço do Exchange expõe essa propriedade. 
  
Você pode recuperar essa propriedade por meio de uma chamada para [IMAPIProp::GetProps](imapiprop-getprops.md) em **PidTagExchangeProfileSectionId** após consultar qualquer uma das seguintes interfaces: 
  
- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Se o objeto não estiver associado ao Exchange, a chamada retornará **MAPI_E_NOT_FOUND**.
  
Você pode restringir contêineres em **um PidTagExchangeProfileSectionId** ao exibir o livro de endereços. Depois de abrir um contêiner, você poderá consultar **o emsmdbUID** a partir dele. Também vale a pena notar que, se um destinatário foi selecionado de um livro de endereços do Exchange, o destinatário também tem o **PidTagExchangeProfileSectionId** em sua lista de propriedades. 
  
> [!NOTE]
> Em todos os exemplos de código e de função, esse GUID é conhecido como **emsmdbUID**. 
  
Uma das contas do Exchange é marcada como a conta herdado do Exchange. Normalmente, é a primeira conta adicionada ao perfil. Cada chamada para abrir **pbGlobalProfileSectionGuid** é redirecionada para a seção global do Exchange da conta herdada. As chamadas de modelo de objeto que interagem com a conta do Exchange não herdado também interagem com a conta herdado do Exchange. 
  
O serviço Exchange herdado tem a propriedade **PR_EMSMDB_LEGACY** (0x3D18000B), que é definida como **true** na tabela de serviços de mensagens. 
  
O **emsmdbUID** herdado também é carimbado na Seção de Perfil Global do Outlook do perfil como **PidTagExchangeProfileSectionId**. O código escrito para dar suporte a várias contas do Exchange não deve ter que recuperar o **emsmdbUID** herdado porque ele deve obter o **emsmdbUID** correto, dependendo da conta com a que seu código está interagindo.
  
## <a name="see-also"></a>Confira também



[Usar várias contas do Exchange](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

