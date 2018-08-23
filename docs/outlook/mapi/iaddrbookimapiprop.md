---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 44bc6de420953bd665bd3caa336b76b15c1effd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579456"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Oferece suporte ao acesso ao catálogo de endereços MAPI e inclui operações como exibir caixas de diálogo comuns; contêineres de abertura, mensagens de usuários e listas de distribuição; e executar a resolução de nome.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Expostos pelo:  <br/> |Objetos de catálogo de endereços  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos clientes, provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IAddrBook  <br/> |
|Tipo de ponteiro:  <br/> |LPADRBOOK  <br/> |
|Modelo de transação:  <br/> |Não gravável  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Abre uma entrada do catálogo de endereços e retorna um ponteiro para uma interface que pode ser usada para acessar a entrada.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Compara dois identificadores de entrada que pertencem a um provedor de catálogo de endereço específico para determinar se eles se referem ao mesmo objeto de catálogo de endereços.  <br/> |
|[Aviso](iaddrbook-advise.md) <br/> |Registra um provedor de serviço ou cliente para receber notificações sobre alterações em uma ou mais entradas no catálogo de endereços.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Cancela um registro de notificação que tenha estabelecido para uma entrada do catálogo de endereços.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Cria um identificador de entrada para um endereço one-off.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Adiciona um novo destinatário para um contêiner de catálogo de endereços ou a lista de destinatários de uma mensagem de saída.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Executa a resolução de nomes, atribuindo identificadores de entrada para destinatários em uma lista de destinatários.  <br/> |
|[Endereço](iaddrbook-address.md) <br/> |Exibe a caixa de diálogo do catálogo de endereços do Outlook.  <br/> |
|[Detalhes](iaddrbook-details.md) <br/> |Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada de catálogo de endereço específica.  <br/> |
|**RecipOptions** <br/> | *Não tem suporte ou documentadas.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Não tem suporte ou documentadas.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Retorna o identificador de entrada do contêiner que é designado como o catálogo de endereços pessoal (PAB).  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Designa um contêiner específico como o catálogo de endereços pessoal (PAB).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Retorna o identificador de entrada para o contêiner de catálogo de endereços inicial.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Estabelece o contêiner especificado como o contêiner de catálogo de endereços padrão que inicialmente é disponibilizado.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Retorna uma lista ordenada de identificadores de entrada dos contêineres a serem incluídos no processo de resolução de nome iniciado pelo método [ResolveName](iaddrbook-resolvename.md) .  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Define um novo caminho de pesquisa no perfil que é usado para o processo de resolução de nome.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

