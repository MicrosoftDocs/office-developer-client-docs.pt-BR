---
title: Assegurando espaço suficiente do TempDBS
TOCTitle: Ensuring Sufficient TempDB Space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 886db9f42f44bd1df4acb678cb969b6d81a64df8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463070"
---
# <a name="ensuring-sufficient-tempdb-space"></a>Assegurando espaço suficiente do TempDBS


**Aplica-se a**: Access 2013 | Office 2013

Se ocorrerem erros ao manipular os objetos [Recordset](recordset-object-ado.md) que precisam de espaço de processamento no Microsoft SQL Server 6.5, pode ser necessário aumentar o tamanho do TempDB. (Algumas consultas requerem espaço de processamento temporário; por exemplo, uma consulta com uma cláusula ORDER BY requer um tipo de **Recordset**, que requer algum espaço temporário.)


> [!IMPORTANT]
> <P>[!IMPORTANTE] Leia esse procedimento antes executar as ações porque isso não é tão fácil quando reduzir um dispositivo depois de ser expandido.</P>




> [!NOTE]
> <P>[!OBSERVAçãO] Por padrão, no Microsoft SQL Server 7.0 e posteriores, o TempDB é definido para aumentar automaticamente conforme necessário. Portanto, esse procedimento pode ser necessário apenas nos servidores que executam versões anteriores à 7.0.</P>



**Para aumentar o espaço do TempDB no SQL Server 6.5**

1.  Inicie o Microsoft® SQL Server Enterprise Manager, abra a árvore para o Server e, em seguida, abra a árvore Database Devices.

2.  Selecione um dispositivo (físico) a ser expandido, como Master, e dê um clique duplo no dispositivo para abrir a caixa de diálogo **Editar dispositivo do banco de dados**. Essa caixa de diálogo mostra quanto espaço os bancos de dados atuais estão usando.

3.  Na caixa **Tamanho**, aumente o dispositivo para a quantidade desejada (por exemplo, 50 MB de espaço em disco rígido).

4.  Clique em **Alterar Agora** para aumentar a quantidade de espaço para o qual o TempDB (lógico) pode ser expandido.

5.  Abra a árvore Banco de Dados no servidor e, em seguida, dê um clique duplo em **TempDB** para abrir a caixa de diálogo **Editar Banco de Dados**. A guia **Banco de Dados** lista a quantidade de espaço atualmente alocada em TempDB (**Data Size**). Por padrão, é 2 MB.

6.  No grupo **Tamanho**, clique em **Expandir**. Os gráficos mostram o espaço disponível e alocado em cada um dos dispositivos físicos. As barras em marrom representam o espaço disponível.

7.  Selecione um **Dispositivo de Log**, como Master, para exibir o tamanho disponível na caixa **Tamanho (MB)**.

8.  Clique em **Expandir Agora** para alocar esse espaço para o banco de dados TempDB. A caixa de diálogo **Editar Banco de Dados** exibe o novo tamanho alocado para TempDB.

Para obter mais informações sobre esse tópico, procure pelo arquivo Microsoft SQL Server Enterprise Manager Help para "caixa de diálogo Expandir Banco de Dados".
