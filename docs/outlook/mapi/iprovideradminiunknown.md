---
title: IProviderAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin
api_type:
- COM
ms.assetid: bdb4cdca-8dfd-4f90-9467-ec31cea3f518
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bedec72e8371d0e8aa69415d2f0dc77b4c62ff76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315523"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Funciona com provedores de serviços em um serviço de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objetos de administração de provedor  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IProviderAdmin  <br/> |
|Tipo de ponteiro:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu com o objeto de administração de provedor.  <br/> |
|[GetProvidertable](iprovideradmin-getprovidertable.md) <br/> |Fornece acesso à tabela do provedor do serviço de mensagens, uma lista dos provedores de serviços no serviço de mensagens.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Adiciona um provedor de serviços ao serviço de mensagens.  <br/> |
|[Deleteprovider](iprovideradmin-deleteprovider.md) <br/> |Exclui um provedor de serviços do serviço de mensagens.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Abre uma seção de perfil do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso.  <br/> |
   
## <a name="remarks"></a>Comentários

Os clientes podem obter um ponteiro para uma interface **IProviderAdmin** chamando o método [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) ; os provedores de serviços recebem um ponteiro **IProviderAdmin** quando a função de ponto de entrada do serviço de mensagens é chamada. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

