---
title: Assegurando espaço suficiente do TempDBS
TOCTitle: Ensuring Sufficient TempDB Space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d049a098a7f7cfd826c6c5945c71831acbceb04
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863049"
---
# <a name="ensuring-sufficient-tempdb-space"></a><span data-ttu-id="6f897-102">Assegurando espaço suficiente do TempDBS</span><span class="sxs-lookup"><span data-stu-id="6f897-102">Ensuring Sufficient TempDB Space</span></span>


<span data-ttu-id="6f897-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f897-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6f897-p101">Se ocorrerem erros ao manipular os objetos [Recordset](recordset-object-ado.md) que precisam de espaço de processamento no Microsoft SQL Server 6.5, pode ser necessário aumentar o tamanho do TempDB. (Algumas consultas requerem espaço de processamento temporário; por exemplo, uma consulta com uma cláusula ORDER BY requer um tipo de **Recordset**, que requer algum espaço temporário.)</span><span class="sxs-lookup"><span data-stu-id="6f897-p101">If errors occur while handling [Recordset](recordset-object-ado.md) objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB. (Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the **Recordset**, which requires some temporary space.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f897-106">[!IMPORTANTE] Leia esse procedimento antes executar as ações porque isso não é tão fácil quando reduzir um dispositivo depois de ser expandido.</span><span class="sxs-lookup"><span data-stu-id="6f897-106">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</span></span>

> [!NOTE]
> <span data-ttu-id="6f897-p102">[!OBSERVAçãO] Por padrão, no Microsoft SQL Server 7.0 e posteriores, o TempDB é definido para aumentar automaticamente conforme necessário. Portanto, esse procedimento pode ser necessário apenas nos servidores que executam versões anteriores à 7.0.</span><span class="sxs-lookup"><span data-stu-id="6f897-p102">By default in Microsoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed. Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</span></span>



<span data-ttu-id="6f897-109">**Para aumentar o espaço do TempDB no SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="6f897-109">**To increase the TempDB space on SQL Server 6.5**</span></span>

1.  <span data-ttu-id="6f897-110">Inicie o Microsoft® SQL Server Enterprise Manager, abra a árvore para o Server e, em seguida, abra a árvore Database Devices.</span><span class="sxs-lookup"><span data-stu-id="6f897-110">Start Microsoft® SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="6f897-p103">Selecione um dispositivo (físico) a ser expandido, como Master, e dê um clique duplo no dispositivo para abrir a caixa de diálogo **Editar dispositivo do banco de dados**. Essa caixa de diálogo mostra quanto espaço os bancos de dados atuais estão usando.</span><span class="sxs-lookup"><span data-stu-id="6f897-p103">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box. This dialog box shows how much space the current databases are using.</span></span>

3.  <span data-ttu-id="6f897-113">Na caixa **Tamanho**, aumente o dispositivo para a quantidade desejada (por exemplo, 50 MB de espaço em disco rígido).</span><span class="sxs-lookup"><span data-stu-id="6f897-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span></span>

4.  <span data-ttu-id="6f897-114">Clique em **Alterar Agora** para aumentar a quantidade de espaço para o qual o TempDB (lógico) pode ser expandido.</span><span class="sxs-lookup"><span data-stu-id="6f897-114">Click **Change Now** to increase the amount of space to which the (logical) TempDB can expand.</span></span>

5.  <span data-ttu-id="6f897-p104">Abra a árvore Banco de Dados no servidor e, em seguida, dê um clique duplo em **TempDB** para abrir a caixa de diálogo **Editar Banco de Dados**. A guia **Banco de Dados** lista a quantidade de espaço atualmente alocada em TempDB (**Data Size**). Por padrão, é 2 MB.</span><span class="sxs-lookup"><span data-stu-id="6f897-p104">Open the Databases tree on the server, and then double-click **TempDB** to open the **Edit Database** dialog box. The **Database** tab lists the amount of space currently allocated to TempDB (**Data Size**). By default, this is 2 MB.</span></span>

6.  <span data-ttu-id="6f897-p105">No grupo **Tamanho**, clique em **Expandir**. Os gráficos mostram o espaço disponível e alocado em cada um dos dispositivos físicos. As barras em marrom representam o espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="6f897-p105">Under the **Size** group, click **Expand**. The graphs show the available and allocated space on each of the physical devices. The bars in maroon color represent available space.</span></span>

7.  <span data-ttu-id="6f897-121">Selecione um **Dispositivo de Log**, como Master, para exibir o tamanho disponível na caixa **Tamanho (MB)**.</span><span class="sxs-lookup"><span data-stu-id="6f897-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span></span>

8.  <span data-ttu-id="6f897-p106">Clique em **Expandir Agora** para alocar esse espaço para o banco de dados TempDB. A caixa de diálogo **Editar Banco de Dados** exibe o novo tamanho alocado para TempDB.</span><span class="sxs-lookup"><span data-stu-id="6f897-p106">Click **Expand Now** to allocate that space to the TempDB database. The **Edit Database** dialog box displays the new allocated size for TempDB.</span></span>

<span data-ttu-id="6f897-124">Para obter mais informações sobre esse tópico, procure pelo arquivo Microsoft SQL Server Enterprise Manager Help para "caixa de diálogo Expandir Banco de Dados".</span><span class="sxs-lookup"><span data-stu-id="6f897-124">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</span></span>

