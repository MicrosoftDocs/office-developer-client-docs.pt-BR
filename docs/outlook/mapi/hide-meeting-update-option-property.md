---
title: Ocultar as propriedades de opção de atualização de reuniões
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 65255e14fd849d730e92bd86027642eef2c687bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584972"
---
# <a name="hide-meeting-update-option-property"></a>Ocultar as propriedades de opção de atualização de reuniões

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Oculta a opção para enviar atualizações de reunião para apenas os participantes adicionados ou excluídos.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Expostas no:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Criados por:  <br/> |Provedor de armazenamento  <br/> |
|Acessado por:  <br/> |Outlook e outros clientes  <br/> |
|Tipo de propriedade:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acesso:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Comentários

Para fornecer qualquer funcionalidade loja, o provedor de repositório deve implementar [IMAPIProp: IUnknown](imapipropiunknown.md) e retornar uma marca de propriedade válido para qualquer uma dessas propriedades passados para uma chamada [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Quando a marca de propriedade para qualquer uma dessas propriedades é passada para [IMAPIProp::GetProps](imapiprop-getprops.md), o provedor de armazenamento também deve retornar o valor da propriedade correto. Provedores de armazenamento podem chamar [HrGetOneProp](hrgetoneprop.md) e [HrSetOneProp](hrsetoneprop.md) para obter ou definir essas propriedades. 
  
Para recuperar o valor dessa propriedade, o cliente deve primeiro usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade e especifique nesta marca de propriedade em [IMAPIProp::GetProps](imapiprop-getprops.md) para obter o valor. Ao chamar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique os seguintes valores para a estrutura [MAPINAMEID](mapinameid.md) apontado pelo parâmetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "urn: schemas-microsoft-com:office:outlook #allornonemtgupdatedlg"  <br/> |
   
Um provedor de armazenamento que usa um servidor para enviar atualizações de reunião pode modificar a caixa de diálogo **Enviar atualização aos participantes** . Essa funcionalidade é útil porque quando o servidor envia uma atualização de reunião, o servidor não saber quais participantes foram adicionados ou excluídos pelo usuário desde a solicitação de reunião inicial. Quando essa propriedade for **true**, a opção **Enviar atualização apenas aos participantes adicionados ou excluídos** não é exibida na caixa de diálogo **Enviar atualização aos participantes** . 
  
Essa propriedade é ignorada se a versão do Outlook é anterior ao Microsoft Office Outlook 2003 Service Pack 1 ou se seu valor for **false**.
  

