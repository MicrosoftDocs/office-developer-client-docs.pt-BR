---
title: Minimizando o uso do espaço do arquivo de log
TOCTitle: Minimizing Log File Space Usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ac2bee2bf3f1036583bd195edc0c3da9e052f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465285"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="8165a-102">Minimizando o uso do espaço do arquivo de log</span><span class="sxs-lookup"><span data-stu-id="8165a-102">Minimizing Log File Space Usage</span></span>


<span data-ttu-id="8165a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8165a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8165a-p101">Um arquivo de log pode preencher rapidamente (parando, assim, o servidor) se houver um grande volume de atividade em um banco de dados do SQL Server. Você pode definir o arquivo de log como **Truncar no Ponto de Verificação** para ampliar significativamente a vida do arquivo de log para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8165a-p101">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="8165a-106">**Para ativar a opção Truncar no Ponto de Verificação no Microsoft SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="8165a-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="8165a-107">Inicie o Microsoft SQL Server Enterprise Manager, abra a árvore do Server e, em seguida, abra a árvore Dispositivos do Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="8165a-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="8165a-108">Clique duas vezes no nome do banco de dados no qual este recurso será ativado.</span><span class="sxs-lookup"><span data-stu-id="8165a-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="8165a-109">Na guia **Banco de Dados**, selecione **Truncar**.</span><span class="sxs-lookup"><span data-stu-id="8165a-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="8165a-110">Na guia **Opções**, selecione **Truncar Log no Ponto de Verificação** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8165a-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="8165a-111">**Para ativar a opção Truncar no Ponto de Verificação no Microsoft SQL Server 7.0**</span><span class="sxs-lookup"><span data-stu-id="8165a-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="8165a-112">Inicie o Microsoft SQL Server Enterprise Manager, abra a árvore do Server e, em seguida, abra a árvore Dispositivos do Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="8165a-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="8165a-113">Clique com o botão direito do mouse no nome do banco de dados no qual este recurso será ativado e escolha **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="8165a-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="8165a-114">Na guia **Opções**, selecione **Truncar Log no Ponto de Verificação** e, em seguida, clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="8165a-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="8165a-115">Para obter mais informações sobre o recurso **Truncar no Ponto de Verificação**, consulte a documentação do Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8165a-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

