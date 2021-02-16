---
title: Propriedade Tornar Tipo de Loja Particular
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428540"
---
# <a name="make-store-type-private-property"></a>Propriedade Tornar Tipo de Loja Particular

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Trata um armazenamento secundário como particular.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exposto em:  <br/> |[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Criado por:  <br/> |Provedor da Loja  <br/> |
|Acessado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Comentários

Para fornecer qualquer uma das funcionalidades do repositório, o provedor de repositório deve implementar [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) e retornar uma marca de propriedade válida para qualquer uma dessas propriedades passadas para uma chamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Quando a marca de propriedade de qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor de propriedade correto. Os provedores da loja podem [chamar HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e, em seguida, especificar essa marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor. Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a [estrutura MAPINAMEID](mapinameid.md) apontada pelo parâmetro de entrada  _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"  <br/> |
   
Um provedor de armazenamento pode usar essa propriedade para que o Outlook o trate como particular quando for um armazenamento secundário para um usuário. 
  
Por padrão, o Outlook trata um armazenamento secundário da mesma forma que um armazenamento delegado, e os itens no armazenamento secundário são particulares somente se o usuário os marcar especificamente como particulares. Quando essa propriedade for **verdadeira, os** itens excluídos  de um armazenamento secundário serão movidos para a pasta Itens Excluídos no armazenamento principal. Itens marcados como particulares não são exibidos. Rascunhos são armazenados na pasta Rascunhos no armazenamento principal. 
  
Essa propriedade será ignorada se a versão do Outlook for anterior ao Microsoft Office Outlook 2003 Service Pack 1 ou se seu valor for **falso.**
  

