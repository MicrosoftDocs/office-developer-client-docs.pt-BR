---
title: Concedendo privilégios de convidados a um computador do servidor Web; Privilégios de convidados RDS
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d09de280c9edcfdf4305bb6c2ba09aa01e556ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463930"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Concedendo privilégios de convidados a um computador do servidor Web; Privilégios de convidados RDS 


**Aplica-se a**: Access 2013 | Office 2013

A conta do servidor Web anônima (IUSR\_*ComputerName*) devem ser adicionados para o grupo local convidados no computador do servidor Web para usar o RDS.

**Para conceder privilégios de convidados a um computador do servidor Web**

1.  No computador do servidor Microsoft Windows® 2000, clique em **Iniciar**, aponte para **Programas**, para **Ferramentas Administrativas** e, em seguida, clique em **Gerenciamento do Computador**.

2.  Na árvore do console, em **Grupos e Usuários Locais**, clique em **Grupos**.

3.  Selecione o grupo local **Convidados**. No menu **Ação**, clique em **Propriedades**.

4.  Na caixa de diálogo **Propriedades dos Convidados**, clique em **Adicionar**.

5.  Se a conta do servidor Web anônima não aparecer na lista da caixa de diálogo **Selecionar usuários ou grupos** , digite seu nome (IUSR\_*ComputerName*) na parte inferior em branco caixa e clique em **Adicionar**.

6.  Clique em **OK**.

