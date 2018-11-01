---
title: Concedendo privilégios de convidados a um computador do servidor Web; Privilégios de convidados RDS
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed450913c7512e8ef20983484ca4b874878fd791
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867164"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Concedendo privilégios de convidados a um computador do servidor Web; Privilégios de convidados RDS 


**Aplica-se a**: Access 2013, o Office 2013

Conta do servidor web anônima (IUSR\_*ComputerName*) devem ser adicionados para o grupo local convidados no computador do servidor web para usar o RDS.

**Para conceder privilégios de convidados a um computador servidor web**

1.  No computador do servidor Microsoft Windows® 2000, clique em **Iniciar**, aponte para **Programas**, para **Ferramentas Administrativas** e, em seguida, clique em **Gerenciamento do Computador**.

2.  Na árvore do console, em **Grupos e Usuários Locais**, clique em **Grupos**.

3.  Selecione o grupo local **Convidados**. No menu **Ação**, clique em **Propriedades**.

4.  Na caixa de diálogo **Propriedades dos Convidados**, clique em **Adicionar**.

5.  Se a conta do servidor de web anônimo não aparecer na lista da caixa de diálogo **Selecionar usuários ou grupos** , digite seu nome (IUSR\_*ComputerName*) na parte inferior em branco caixa e clique em **Adicionar**.

6.  Clique em **OK**.

