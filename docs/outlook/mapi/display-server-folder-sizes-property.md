---
title: Exibir a propriedade Tamanhos de Pasta do Servidor
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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434547"
---
# <a name="display-server-folder-sizes-property"></a>Exibir a propriedade Tamanhos de Pasta do Servidor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe os tamanhos das pastas especificadas no servidor na caixa de diálogo Tamanho da Pasta **do** Outlook. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exposto em:  <br/> |[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Criado por:  <br/> |Provedor da Loja  <br/> |
|Acessado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Comentários

Para fornecer qualquer uma das funcionalidades do armazenamento, o provedor de armazenamento deve implementar [IMAPIProp : IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Quando a marca de propriedade de qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor de propriedade correto. Os provedores da loja podem [chamar HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor. Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a [estrutura MAPINAMEID](mapinameid.md) apontada pelo parâmetro de entrada  _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"  <br/> |
   
Essa propriedade é suportada no Microsoft Outlook 2003 Service Pack (SP) 1. Se a versão do Outlook for anterior ao Outlook 2003 SP 1 ou se seu valor for **falso,** o Outlook exibirá apenas os tamanhos de pastas no armazenamento local. Se essa propriedade for definida em um armazenamento que usa o Outlook 2003 SP 1, o Outlook consultará o tamanho de cada pasta especificada no servidor e na unidade local. 
  
To query for the folder size on the server, Outlook opens a folder on the store with [IMsgStore::OpenEntry](imsgstore-openentry.md), passing the flag **MAPI_NO_CACHE**, and then itries for **PR_MESSAGE_SIZE_EXTENDED**. Em seguida, o provedor de armazenamento deve retornar o tamanho da pasta no servidor.
  
Para consultar o tamanho de uma pasta na unidade local, o Outlook abre a pasta sem o **sinalizador MAPI_NO_CACHE** local. Em seguida, ele **consulta** PR_MESSAGE_SIZE_EXTENDED ; o provedor de armazenamento deve retornar o tamanho da pasta especificada na unidade local.
  
Com esse conjunto de propriedades, os provedores de armazenamento que sincronizam o conteúdo do armazenamento com um servidor podem exibir dados de tamanho de pasta no servidor na caixa de diálogo Tamanho da Pasta **do** Outlook. Os usuários podem então comparar o uso atual do armazenamento do servidor com as cotas do servidor. 
  

