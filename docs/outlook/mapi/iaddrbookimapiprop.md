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
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429821"
---
# <a name="iaddrbook--imapiprop"></a>IAddrBook : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Dá suporte ao acesso ao livro de endereços MAPI e inclui operações como exibir caixas de diálogo comuns; abrir contêineres, usuários de mensagens e listas de distribuição; e executando a resolução de nomes.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Exposto por:  <br/> |Objetos do livro de endereços  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente, provedores de serviços  <br/> |
|Identificador de interface:  <br/> |IID_IAddrBook  <br/> |
|Tipo de ponteiro:  <br/> |LPADRBOOK  <br/> |
|Modelo de transação:  <br/> |Não pode ser escrito  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[OpenEntry](iaddrbook-openentry.md) <br/> |Abre uma entrada do livro de endereços e retorna um ponteiro para uma interface que pode ser usada para acessar a entrada.  <br/> |
|[CompareEntryIDs](iaddrbook-compareentryids.md) <br/> |Compara dois identificadores de entrada que pertencem a um provedor de agendas específica para determinar se eles se referem ao mesmo objeto do livro de endereços.  <br/> |
|[Advise](iaddrbook-advise.md) <br/> |Registra um cliente ou provedor de serviços para receber notificações sobre alterações em uma ou mais entradas no livro de endereços.  <br/> |
|[Unadvise](iaddrbook-unadvise.md) <br/> |Cancela um registro de notificação estabelecido anteriormente para uma entrada do livro de endereços.  <br/> |
|[CreateOneOff](iaddrbook-createoneoff.md) <br/> |Cria um identificador de entrada para um endereço único.  <br/> |
|[NewEntry](iaddrbook-newentry.md) <br/> |Adiciona um novo destinatário a um contêiner de livro de endereços ou à lista de destinatários de uma mensagem de saída.  <br/> |
|[ResolveName](iaddrbook-resolvename.md) <br/> |Executa a resolução de nomes, atribuindo identificadores de entrada a destinatários em uma lista de destinatários.  <br/> |
|[Endereço](iaddrbook-address.md) <br/> |Exibe a caixa de diálogo do livro de endereços do Outlook.  <br/> |
|[Detalhes](iaddrbook-details.md) <br/> |Exibe uma caixa de diálogo que mostra detalhes sobre uma entrada específica do livro de endereços.  <br/> |
|**RecipOptions** <br/> | *Sem suporte ou documentado.*  <br/> |
|**QueryDefaultRecipOpt** <br/> | *Sem suporte ou documentado.*  <br/> |
|[GetPAB](iaddrbook-getpab.md) <br/> |Retorna o identificador de entrada do contêiner designado como o pab (lista de endereços pessoal).  <br/> |
|[SetPAB](iaddrbook-setpab.md) <br/> |Designa um contêiner específico como o pab (lista de endereços pessoal).  <br/> |
|[GetDefaultDir](iaddrbook-getdefaultdir.md) <br/> |Retorna o identificador de entrada para o contêiner inicial do agendador de endereços.  <br/> |
|[SetDefaultDir](iaddrbook-setdefaultdir.md) <br/> |Estabelece o contêiner especificado como o contêiner de agendamento padrão que é inicialmente disponibilizado.  <br/> |
|[GetSearchPath](iaddrbook-getsearchpath.md) <br/> |Retorna uma lista ordenada de identificadores de entrada dos contêineres a serem incluídos no processo de resolução de nomes iniciado pelo [método ResolveName.](iaddrbook-resolvename.md)  <br/> |
|[SetSearchPath](iaddrbook-setsearchpath.md) <br/> |Define um novo caminho de pesquisa no perfil usado para o processo de resolução de nomes.  <br/> |
|[PrepareRecips](iaddrbook-preparerecips.md) <br/> |Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

