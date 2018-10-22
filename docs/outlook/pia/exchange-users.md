---
title: Usuários do Exchange
TOCTitle: Exchange users
ms:assetid: 01802032-fd60-400b-ad83-1f4eefe596bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184585(v=office.15)
ms:contentKeyID: 55119835
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 775bfa2c67f3f570bddc749fb995460f6b90b18a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406985"
---
# <a name="exchange-users"></a>Usuários do Exchange

Esta seção fornece tarefas de exemplo que envolvem usuários de caixa de correio do Microsoft Exchange. Os usuários do Exchange estão conectados a um servidor Exchange e são representados pelos objetos [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), derivados do objeto [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)).

## <a name="in-this-section"></a>Nesta seção

|Tópico|Descrição|
|:----|:----------|
|[Acessar informações sobre o usuário atual](how-to-get-information-about-the-current-user.md)  |Tem acesso a informações do usuário, como nome, cargo e número de telefone.|
|[Obter informações sobre todas as listas de distribuição das quais o usuário atual participa](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)  |Usa o método [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) para obter informações sobre todas as listas de distribuição das quais o usuário atual participa.|
|[Criar uma lista de distribuição](how-to-create-a-distribution-list.md)  |Cria uma lista de distribuição e exibe-a ao usuário.|
[Obter membros de uma lista de distribuição do Exchange](how-to-get-members-of-an-exchange-distribution-list.md)  |Solicita que o usuário escolha uma lista de distribuição do Exchange na caixa de diálogo **Selecionar Nomes** e expanda a lista de distribuição para exibir seus membros.|
[Acessar informações sobre o gerente do usuário atual](how-to-get-information-about-the-current-user-s-manager.md)  |Tem acesso a informações (como nome, cargo e número de telefone) do gerente do usuário atual.|
[Ter informações de disponibilidade do gerente de um usuário Exchange](how-to-get-availability-information-for-an-exchange-user-s-manager.md) |  Exibe o próximo intervalo de tempo de 60 minutos gratuitos no calendário para o gerente de um usuário.|
|[Verificar a resposta do gerente para uma solicitação de reunião](how-to-check-a-manager-s-response-to-a-meeting-request.md) | Usa os métodos [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) e [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) para verificar o status da resposta do gerente do usuário atual para uma solicitação de reunião.|
|[Obter informações sobre subordinados diretos do gerente do usuário atual ](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md) | Recebe os subordinados diretos do gerente atual do usuário, se houver algum, e exibe informações sobre cada um deles.|

## <a name="see-also"></a>Confira também

- [Contas](accounts.md)
- [Catálogo de endereços](address-book.md)
- [Repositórios](stores.md)
- [Como faço para... (Referência do Outlook 2013 PIA)](how-do-i-outlook-2013-pia-reference.md)

