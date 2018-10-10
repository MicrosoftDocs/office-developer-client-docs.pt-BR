---
title: Visão geral do objeto Command
TOCTitle: Command Object Overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1e6cd3b2ebea67fac7cef7e556038490b3eb9b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465122"
---
# <a name="command-object-overview"></a><span data-ttu-id="f26a3-102">Visão geral do objeto Command</span><span class="sxs-lookup"><span data-stu-id="f26a3-102">Command Object Overview</span></span>


<span data-ttu-id="f26a3-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f26a3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f26a3-104">Com as coleções, os métodos e as propriedades de um objeto **Command**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="f26a3-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="f26a3-105">Definir o texto executável do comando (por exemplo, uma instrução SQL ou um procedimento armazenado) usando a propriedade **CommandText**.</span><span class="sxs-lookup"><span data-stu-id="f26a3-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="f26a3-106">Definir consultas com parâmetros ou argumentos de procedimentos armazenados usando objetos **Parameter** e a coleção **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="f26a3-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="f26a3-107">Executar um comando e retornar um objeto **Recordset**, se adequado, usando o método **Execute**.</span><span class="sxs-lookup"><span data-stu-id="f26a3-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="f26a3-108">Especificar o tipo de comando usando a propriedade **CommandType** antes da execução, para otimizar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="f26a3-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="f26a3-109">Controlar se o provedor salva uma versão preparada (ou compilada) do comando antes da execução usando a propriedade **Prepared**.</span><span class="sxs-lookup"><span data-stu-id="f26a3-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="f26a3-110">Definir o número de segundos que um provedor irá aguardar até a execução de um comando usando a propriedade **CommandTimeout**.</span><span class="sxs-lookup"><span data-stu-id="f26a3-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="f26a3-111">Associar uma conexão aberta a um objeto **Command** definindo sua propriedade **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="f26a3-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="f26a3-112">Definir a propriedade **Name** para identificar o objeto **Command** como um método no objeto **Connection** associado.</span><span class="sxs-lookup"><span data-stu-id="f26a3-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="f26a3-113">Passar um objeto **Command** para a propriedade **Source** de um **Recordset** para obter dados.</span><span class="sxs-lookup"><span data-stu-id="f26a3-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>

