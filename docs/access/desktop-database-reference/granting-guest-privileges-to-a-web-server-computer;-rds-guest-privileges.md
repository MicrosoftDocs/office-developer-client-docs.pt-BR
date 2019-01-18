---
title: Concedendo privilégios de convidados a um computador do servidor web; Privilégios de convidados RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700546"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Concedendo privilégios de convidados a um computador do servidor web; Privilégios de convidados RDS

**Aplica-se a**: Access 2013, o Office 2013

Conta do servidor web anônima (IUSR\_*ComputerName*) devem ser adicionados para o grupo local convidados no computador do servidor web para usar o RDS.

**Para conceder privilégios de convidados a um computador servidor web**

1.  No computador do Microsoft Windows 2000 Server, clique em **Iniciar**, aponte para **programas**, aponte para **Ferramentas administrativas**e, em seguida, clique em **Gerenciamento do computador**.

2.  Na árvore do console, em **Grupos e Usuários Locais**, clique em **Grupos**.

3.  Selecione o grupo local **Convidados**. No menu **Ação**, clique em **Propriedades**.

4.  Na caixa de diálogo **Propriedades dos Convidados**, clique em **Adicionar**.

5.  Se a conta do servidor de web anônimo não aparecer na lista da caixa de diálogo **Selecionar usuários ou grupos** , digite seu nome (IUSR\_*ComputerName*) na parte inferior em branco caixa e clique em **Adicionar**.

6.  Clique em **OK**.

