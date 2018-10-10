---
title: Prevendo erros
TOCTitle: Anticipating Errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f062eb86b45778cc7f25fb2d0d0588b82bdd78b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464576"
---
# <a name="anticipating-errors"></a>Prevendo erros


**Aplica-se a**: Access 2013 | Office 2013

A prevenção de erros é tão importante quanto o tratamento de erros. Esta seção final contém uma pequena lista de precauções que podem ser tomadas pelo aplicativo para ajudar a diminuir a probabilidade de ocorrência de erros.

Confira o estado dos objetos verificando o valor da propriedade **State** antes de tentar executar uma operação usando esses objetos. Por exemplo, se o aplicativo usar uma **Conexão** global, verifique a respectiva propriedade **State** para ver se ela já está aberta, antes de chamar o método **Open**.

  - Qualquer programa que aceite dados de um usuário deve incluir código para validar esses dados antes de enviá-los para o repositório. Você não pode contar com o repositório de dados, o provedor, o ADO ou mesmo a sua linguagem de programação para notificá-lo de problemas. É necessário verificar cada byte inserido pelos seus usuários, para ter certeza de que os dados são do tipo correto para o campo e que os campos obrigatórios não estão vazios.

Verifique os dados antes de tentar gravá-los no repositório. A maneira mais fácil de fazer isso é manipular o evento **WillMove** ou o evento **WillUpdateRecordset**. Para obter uma abordagem mais completa da manipulação de eventos do ADO, consulte [Capítulo 7: Manipulando eventos do ADO](chapter-7-handling-ado-events.md).

Verifique se os objetos **Recordset** não ultrapassam os limites do **Recordset** antes de tentar mover o ponteiro do registro. Se você tentar **MoveNext** quando **EOF** for True ou tentar **MovePrev** quando **BOF** for True, ocorrerá um erro. Se você executar qualquer um dos métodos **Move** quando **EOF** e **BOF** forem True, será gerado um erro.

Também ocorrerão erros se você tentar executar operações como **Seek** e **Find** em um **Recordset** vazio.

