---
title: Concedendo privilégios de convidado a um computador servidor Web; Privilégios de convidados RDS
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292122"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Concedendo privilégios de convidado a um computador servidor Web; Privilégios de convidados RDS

**Aplica-se ao:** Access 2013, Office 2013

A conta de servidor Web anônima (IUSR ComputerName ) deve ser adicionada ao grupo local Convidados no computador servidor Web para \_ usar o RDS.

**Para conceder privilégios de convidado a um computador servidor Web**

1.  No computador com o Microsoft Windows 2000 Server, clique em **Iniciar,** aponte para **Programas,** aponte para Ferramentas Administrativas e clique em Gerenciamento **do Computador.**

2.  Na árvore do console, em **Grupos e Usuários Locais**, clique em **Grupos**.

3.  Selecione o grupo local **Convidados**. No menu **Ação**, clique em **Propriedades**.

4.  Na caixa de diálogo **Propriedades dos Convidados**, clique em **Adicionar**.

5.  Se a conta de servidor Web anônima  não aparecer na lista na caixa de diálogo Selecionar Usuários ou Grupos, digite seu nome (IUSR \_ *ComputerName*) na caixa em branco inferior e clique em **Adicionar**.

6.  Clique em **OK**.

