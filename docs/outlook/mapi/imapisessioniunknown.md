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
ms.openlocfilehash: a37d8138547c8c4e9308dbb0ebbc6750b152d795
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767207"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Gerencia objetos associados a uma sessão de logon MAPI.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Expostos pelo:  <br/> |Objetos de sessão  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente e MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMAPISession  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de sessão anterior.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Fornece acesso à tabela do repositório de mensagem que contém informações sobre todos os repositórios de mensagem no perfil da sessão.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Abre um armazenamento de mensagens e retorna um ponteiro de [IMsgStore](imsgstoreimapiprop.md) para obter mais acesso.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Abre o catálogo de endereços integrada de MAPI, retornando um ponteiro [IAddrBook](iaddrbookimapiprop.md) para obter mais acesso.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Fornece acesso à tabela de status, uma tabela que contém informações sobre todos os recursos MAPI na sessão.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Abre um objeto e retorna um ponteiro de interface para obter mais acesso.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[Aviso](imapisession-advise.md) <br/> |Registra para receber notificações de eventos especificados que afetam a sessão.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Cancela o envio de notificações configuradas anteriormente com uma chamada ao método **Advise** .  <br/> |
|**MessageOptions** <br/> | *Não tem suporte ou documentadas.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Não tem suporte ou documentadas.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Obsoleto. Retorna os tipos de endereço que podem ser administrados por todos os provedores de transporte na sessão.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Retorna o identificador de entrada do objeto que fornece a identidade principal para a sessão.  <br/> |
|[Fazer logoff](imapisession-logoff.md) <br/> |Finaliza uma sessão MAPI.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Estabelece um armazenamento de mensagens como o armazenamento de mensagens padrão para a sessão.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Retorna um ponteiro [IMsgServiceAdmin](imsgserviceadminiunknown.md) para fazer alterações em serviços de mensagens.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Exibe um formulário.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Cria um token numérico que o método **ShowForm** usa para acessar uma mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

