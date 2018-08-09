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
ms.openlocfilehash: 41195a49d1bf3566c81fe6e97697012209cbc5ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767645"
---
# <a name="iprovideradmin--iunknown"></a>IProviderAdmin : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Funciona com provedores de serviço em um serviço de mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de administração do provedor  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IProviderAdmin  <br/> |
|Tipo de ponteiro:  <br/> |LPPROVIDERADMIN  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](iprovideradmin-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreram com o objeto de administração do provedor.  <br/> |
|[GetProviderTable](iprovideradmin-getprovidertable.md) <br/> |Fornece acesso à tabela do provedor do serviço na mensagem, uma lista dos provedores de serviço no serviço de mensagem.  <br/> |
|[CreateProvider](iprovideradmin-createprovider.md) <br/> |Adiciona um provedor de serviço para o serviço de mensagem.  <br/> |
|[DeleteProvider](iprovideradmin-deleteprovider.md) <br/> |Exclui um provedor de serviço do serviço de mensagem.  <br/> |
|[OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |Abre uma seção de perfil do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso.  <br/> |
   
## <a name="remarks"></a>Comentários

Os clientes podem obter um ponteiro para uma interface **IProviderAdmin** chamando o método [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) ; provedores de serviços são passados um ponteiro **IProviderAdmin** quando a função de ponto de entrada do seu serviço de mensagem é chamada. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

