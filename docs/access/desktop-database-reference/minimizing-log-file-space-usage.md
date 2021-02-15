---
title: Como minimizar o uso de espaço no arquivo de log
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288873"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="4fd77-102">Como minimizar o uso de espaço no arquivo de log</span><span class="sxs-lookup"><span data-stu-id="4fd77-102">Minimizing log file space usage</span></span>

<span data-ttu-id="4fd77-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fd77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4fd77-p101">Um arquivo de log pode preencher rapidamente (parando, assim, o servidor) se houver um grande volume de atividade em um banco de dados do SQL Server. Você pode definir o arquivo de log como **Truncar no Ponto de Verificação** para ampliar significativamente a vida do arquivo de log para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4fd77-p101">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="4fd77-106">**Para ativar a opção Truncar no Ponto de Verificação no Microsoft SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="4fd77-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="4fd77-107">Inicie o Microsoft SQL Server Enterprise Manager, abra a árvore do Server e, em seguida, abra a árvore Dispositivos do Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="4fd77-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="4fd77-108">Clique duas vezes no nome do banco de dados no qual este recurso será ativado.</span><span class="sxs-lookup"><span data-stu-id="4fd77-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="4fd77-109">Na guia **Banco de Dados**, selecione **Truncar**.</span><span class="sxs-lookup"><span data-stu-id="4fd77-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="4fd77-110">Na guia **Opções**, selecione **Truncar Log no Ponto de Verificação** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fd77-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="4fd77-111">**Para ativar a opção Truncar no Ponto de Verificação no Microsoft SQL Server 7.0**</span><span class="sxs-lookup"><span data-stu-id="4fd77-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="4fd77-112">Inicie o Microsoft SQL Server Enterprise Manager, abra a árvore do Server e, em seguida, abra a árvore Dispositivos do Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="4fd77-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="4fd77-113">Clique com o botão direito do mouse no nome do banco de dados no qual este recurso será ativado e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="4fd77-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="4fd77-114">Na guia **Opções**, selecione **Truncar Log no Ponto de Verificação** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fd77-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="4fd77-115">Para obter mais informações sobre o recurso **Truncar no Ponto de Verificação**, consulte a documentação do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4fd77-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

