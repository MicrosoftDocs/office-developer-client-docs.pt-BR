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
ms.openlocfilehash: aba61d4acf7c1f9a5d91fa15f1ca6b16f173bcb2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309706"
---
# <a name="imsgserviceadmin--iunknown"></a>IMsgServiceAdmin : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz alterações em um serviço de mensagens em um perfil.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MapiX. h  <br/> |
|Exposto por:  <br/> |Objetos de administração do serviço de mensagens  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMsgServiceAdmin  <br/> |
|Tipo de ponteiro:  <br/> |LPSERVICEADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](imsgserviceadmin-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro gerado por um objeto de administração do serviço de mensagens.  <br/> |
|[GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) <br/> |Fornece acesso à tabela de serviço de mensagens, uma lista dos serviços de mensagens no perfil.  <br/> |
|[CreateMsgService](imsgserviceadmin-createmsgservice.md) <br/> |Adiciona um serviço de mensagens ao perfil atual.  <br/> <br/>**Observação**: esse método foi preterido. Use [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) em vez disso.           |
|[DeleteMsgService](imsgserviceadmin-deletemsgservice.md) <br/> |Exclui um serviço de mensagens de um perfil.  <br/> |
|[CopyMsgService](imsgserviceadmin-copymsgservice.md) <br/> |Copia um serviço de mensagens em um perfil.  <br/> |
|[RenameMsgService](imsgserviceadmin-renamemsgservice.md) <br/> |Obsoleto. Atribui um novo nome a um serviço de mensagens.  <br/> |
|[ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) <br/> |Reconfigura um serviço de mensagens.  <br/> |
|[OpenProfileSection](imsgserviceadmin-openprofilesection.md) <br/> |Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso.  <br/> |
|[MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) <br/> |Define a ordem na qual os provedores de transporte são chamados para entregar uma mensagem.  <br/> |
|[AdminProviders](imsgserviceadmin-adminproviders.md) <br/> |Retorna um ponteiro que fornece acesso a um objeto de administração de provedor.  <br/> |
|[SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) <br/> |Designa um serviço de mensagem para ser o fornecedor da identidade principal do perfil.  <br/> |
|[GetProvidertable](imsgserviceadmin-getprovidertable.md) <br/> |Fornece acesso à tabela do provedor, uma lista dos provedores de serviços no perfil.  <br/> |
   
## <a name="remarks"></a>Comentários

Uma implementação pode obter um ponteiro para uma interface **IMsgServiceAdmin** de duas maneiras: chamando o método [IMAPISession:: adminservices](imapisession-adminservices.md) ou chamando o método [IProfAdmin:: adminservices](iprofadmin-adminservices.md) . Para os clientes preocupados principalmente com a configuração de perfil, **IProfAdmin:: adminservices** é a melhor maneira de obter a interface **IMsgServiceAdmin** , pois não faz logon nos provedores da sessão MAPI. Se um cliente requer a capacidade de fazer alterações no perfil ativo, **IMAPISession:: adminservices** deve ser chamado para obter o ponteiro **IMsgServiceAdmin** . Lembre-se de que, embora o MAPI não permita que um perfil em uso seja excluído, não há garantias para impedir que um cliente remova todos os serviços de mensagens no perfil. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

