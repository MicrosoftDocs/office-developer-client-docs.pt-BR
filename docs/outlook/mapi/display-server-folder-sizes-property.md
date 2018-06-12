---
title: Propriedade tamanhos da pasta de exibição servidor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1ddf4501918d598169a3a74fd1c8d2ac38499cd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766421"
---
# <a name="display-server-folder-sizes-property"></a>Propriedade tamanhos da pasta de exibição servidor

  
  
**Aplica-se a**: Outlook 
  
Exibe os tamanhos das pastas especificadas no servidor, na caixa de diálogo **Tamanho da pasta** do Outlook. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Expostas no:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Criados por:  <br/> |Provedor de armazenamento  <br/> |
|Acessado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Coment�rios

Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto. Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor. Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "urn: schemas-microsoft-com:office:outlook #serverfoldersizes"  <br/> |
   
Essa propriedade é suportada no Microsoft Outlook 2003 Service Pack (SP) 1. Se a versão do Outlook é anterior ao Outlook 2003 SP 1, ou se seu valor for **false**, o Outlook exibirá apenas os tamanhos das pastas no armazenamento local. Se essa propriedade for definida em um repositório que usa o Outlook 2003 SP 1, o Outlook irá consultar o tamanho de cada pasta especificada no servidor e na unidade local. 
  
Para consultar o tamanho da pasta no servidor, o Outlook abre uma pasta no repositório com [IMsgStore::OpenEntry](imsgstore-openentry.md), passando o sinalizador **MAPI_NO_CACHE**, e, em seguida, ele pede **PR_MESSAGE_SIZE_EXTENDED**. O provedor de armazenamento, em seguida, deve retornar o tamanho da pasta no servidor.
  
Para consultar o tamanho de uma pasta na unidade local, o Outlook abre a pasta sem o sinalizador **MAPI_NO_CACHE** . Ele então consultas para **PR_MESSAGE_SIZE_EXTENDED**; o provedor de armazenamento deve retornar o tamanho da pasta especificada na unidade local.
  
Com essa propriedade é definida, provedores de armazenamento que sincronizar o repositório de conteúdo para um servidor podem exibir dados de tamanho de pasta no servidor, na caixa de diálogo **Tamanho da pasta** do Outlook. Os usuários, em seguida, podem comparar o seu uso de armazenamento do servidor atual com cotas de servidor. 
  

