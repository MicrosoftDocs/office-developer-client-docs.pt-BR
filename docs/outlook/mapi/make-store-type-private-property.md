---
title: Propriedade para tornar privado o tipo de repositório
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
ms.openlocfilehash: 7f60d9524af18bb7f2e876386c45b84f207d42bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767806"
---
# <a name="make-store-type-private-property"></a>Propriedade para tornar privado o tipo de repositório

  
  
**Aplica-se a**: Outlook 
  
Um repositório secundário a tratará como particular.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Expostas no:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Criados por:  <br/> |Provedor de armazenamento  <br/> |
|Acessado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Comentários

Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto. Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor. Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "urn: schemas-microsoft-com:office:outlook #storetypeprivate"  <br/> |
   
Um provedor de armazenamento pode usar essa propriedade para fazer com que o Outlook tratá-lo como privada, quando ele é um repositório secundário para um usuário. 
  
Por padrão, o Outlook trata um repositório secundário da mesma maneira como um repositório representante e itens no armazenamento secundário são particulares somente se o usuário marca-las especificamente como particular. Quando essa propriedade for **true**, os itens excluídos de um repositório secundário são movidos para a pasta **Itens excluídos** no repositório principal. Itens marcados como particulares não são exibidos. Os rascunhos são armazenados na pasta Rascunhos no repositório principal. 
  
Essa propriedade é ignorada se a versão do Outlook é anterior ao Microsoft Office Outlook 2003 Service Pack 1 ou se seu valor for **false**.
  

