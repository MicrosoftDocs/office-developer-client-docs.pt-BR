---
title: IMsgServiceAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin
api_type:
- COM
ms.assetid: 5905b9e9-c462-451d-a49f-1f3a8aa506a6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cf275c66a60ed977c442b468b7c9951325db5120
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593512"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz alterações em um serviço de mensagem em um perfil.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MapiX.h  <br/> |
|Expostos pelo:  <br/> |Objetos de administração do serviço de mensagem  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Tipo de ponteiro:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro gerado por um objeto de administração do serviço de mensagem.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Fornece acesso à tabela de serviço de mensagem, uma lista dos serviços de mensagem no perfil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Adiciona um serviço de mensagem ao perfil atual.  <br/> <br/>**Observação**: esse método foi preterido. Use [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) .           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Exclui um serviço de mensagem de um perfil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Copia um serviço de mensagem para um perfil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Obsoleto. Atribui um novo nome para um serviço de mensagem.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Reconfigura um serviço de mensagem.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Define a ordem na qual transporte provedores são chamados para entregar uma mensagem.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Retorna um ponteiro que fornece acesso a um objeto de administração do provedor.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Designa um serviço de mensagem a ser o fornecedor da identidade principal para o perfil.  <br/> |
|[GetProviderTable](imsgserviceadmin-getprovidertable.md) <br/> |Fornece acesso à tabela de provedor, uma lista de provedores de serviços de perfil.  <br/> |
   
## <a name="remarks"></a>Comentários

Uma implementação pode obter um ponteiro para uma interface **IMsgServiceAdmin** de duas maneiras: chamando o método [IMAPISession::AdminServices](imapisession-adminservices.md) ou chamando o método [IProfAdmin::AdminServices](iprofadmin-adminservices.md) . Para clientes principalmente preocupados com a configuração de perfil, **IProfAdmin::AdminServices** é a maneira preferencial para obter a interface **IMsgServiceAdmin** , pois ele não fazer logon provedores para a sessão MAPI. Se um cliente exigir a capacidade de fazer alterações para o perfil ativo, **IMAPISession::AdminServices** deve ser chamado para obter o ponteiro **IMsgServiceAdmin** . Lembre-se de que, embora MAPI não permitir que um perfil que está em uso a ser excluído, não há nenhuma proteções para impedir que um cliente removendo todos os serviços de mensagem no perfil. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

