---
title: Minimizando o uso do espaço do arquivo de log
TOCTitle: Minimizing Log File Space Usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 119e4bc607296d1a68aef6f85d44f15718940b42
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25866982"
---
# <a name="minimizing-log-file-space-usage"></a>Minimizando o uso do espaço do arquivo de log


**Aplica-se a**: Access 2013, o Office 2013

Um arquivo de log pode preencher rapidamente (parando, assim, o servidor) se houver um grande volume de atividade em um banco de dados do SQL Server. Você pode definir o arquivo de log como **Truncar no Ponto de Verificação** para ampliar significativamente a vida do arquivo de log para um banco de dados.

**Para ativar a opção Truncar no Ponto de Verificação no Microsoft SQL Server 6.5**

1.  Inicie o Microsoft SQL Server Enterprise Manager, abra a árvore do Server e, em seguida, abra a árvore Dispositivos do Banco de Dados.

2.  Clique duas vezes no nome do banco de dados no qual este recurso será ativado.

3.  Na guia **Banco de Dados**, selecione **Truncar**.

4.  Na guia **Opções**, selecione **Truncar Log no Ponto de Verificação** e, em seguida, clique em **OK**.

**Para ativar a opção Truncar no Ponto de Verificação no Microsoft SQL Server 7.0**

1.  Inicie o Microsoft SQL Server Enterprise Manager, abra a árvore do Server e, em seguida, abra a árvore Dispositivos do Banco de Dados.

2.  Clique com o botão direito do mouse no nome do banco de dados no qual este recurso será ativado e escolha **Propriedades**.

3.  Na guia **Opções**, selecione **Truncar Log no Ponto de Verificação** e, em seguida, clique em **OK**.

Para obter mais informações sobre o recurso **Truncar no Ponto de Verificação**, consulte a documentação do Microsoft SQL Server.

