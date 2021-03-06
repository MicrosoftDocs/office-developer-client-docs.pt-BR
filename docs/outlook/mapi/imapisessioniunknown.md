---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413378"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gerencia objetos associados a uma sessão de logon MAPI.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Exposto por:  <br/> |Objetos Session  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISession  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro de sessão anterior.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Fornece acesso à tabela do armazenamento de mensagens que contém informações sobre todos os armazenamentos de mensagens no perfil de sessão.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Abre um repositório de mensagens e retorna um ponteiro [IMsgStore](imsgstoreimapiprop.md) para mais acesso.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Abre o livro de endereços integrado MAPI, retornando um ponteiro [IAddrBook](iaddrbookimapiprop.md) para mais acesso.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para mais acesso.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Fornece acesso à tabela de status, uma tabela que contém informações sobre todos os recursos MAPI na sessão.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Abre um objeto e retorna um ponteiro de interface para mais acesso.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[Advise](imapisession-advise.md) <br/> |Registra para receber notificação de eventos especificados que afetam a sessão.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Cancela o envio de notificações configuradas anteriormente com uma chamada para o **método Advise.**  <br/> |
|**MessageOptions** <br/> | *Sem suporte ou documentado.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Sem suporte ou documentado.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Depreciado. Retorna os tipos de endereço que podem ser manipulados por todos os provedores de transporte na sessão.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Retorna o identificador de entrada do objeto que fornece a identidade principal para a sessão.  <br/> |
|[Fazer logoff](imapisession-logoff.md) <br/> |Encerra uma sessão MAPI.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Estabelece um armazenamento de mensagens como o armazenamento de mensagens padrão para a sessão.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Retorna um [ponteiro IMsgServiceAdmin](imsgserviceadminiunknown.md) para fazer alterações nos serviços de mensagens.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Exibe um formulário.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Cria um token numérico que o **método ShowForm** usa para acessar uma mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

