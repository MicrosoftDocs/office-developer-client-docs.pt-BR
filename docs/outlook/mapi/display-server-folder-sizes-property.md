---
title: Exibir Propriedade tamanhos de pasta do servidor
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337076"
---
# <a name="display-server-folder-sizes-property"></a>Exibir Propriedade tamanhos de pasta do servidor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exibe os tamanhos das pastas especificadas no servidor na caixa de diálogo **tamanho da pasta** do Outlook. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exposto em:  <br/> |[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Criado por:  <br/> |Provedor de repositório  <br/> |
|AcEssado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Comentários

Para fornecer qualquer uma das funcionalidades de armazenamento, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::](imapiprop-getprops.md)GetProps, o provedor de repositório também deve retornar o valor de propriedade correto. Os provedores de repositório podem chamar o [HrGetOneProp](hrgetoneprop.md) e o [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::](imapiprop-getprops.md) GetProps para obter o valor. Ao chamar [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) indicada pelo parâmetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Tipo. lpwstrName:  <br/> |L "urn: schemas-microsoft-com: Office: Outlook # serverfoldersizes"  <br/> |
   
Esta propriedade tem suporte no Microsoft Outlook 2003 Service Pack (SP) 1. Se a versão do Outlook for anterior ao Outlook 2003 SP 1 ou se o valor for **false**, o Outlook exibirá apenas os tamanhos das pastas no repositório local. Se essa propriedade for definida em um repositório que usa o Outlook 2003 SP 1, o Outlook consultará o tamanho de cada pasta especificada no servidor e na unidade local. 
  
Para consultar o tamanho da pasta no servidor, o Outlook abre uma pasta no repositório com [IMsgStore:: OpenEntry](imsgstore-openentry.md), passando o sinalizador **MAPI_NO_CACHE**e, em seguida, consulta o **PR_MESSAGE_SIZE_EXTENDED**. O provedor de repositório deve retornar o tamanho da pasta no servidor.
  
Para consultar o tamanho de uma pasta na unidade local, o Outlook abre a pasta sem o sinalizador **MAPI_NO_CACHE** . Em seguida, ele consulta o **PR_MESSAGE_SIZE_EXTENDED**; o provedor de repositório deve retornar o tamanho da pasta especificada na unidade local.
  
Com esse conjunto de propriedades, os provedores de repositório que sincronizam o conteúdo para um servidor podem exibir dados de tamanho de pasta no servidor na caixa de diálogo **tamanho da pasta** do Outlook. Os usuários podem comparar o uso do armazenamento do servidor atual com as cotas de servidor. 
  

