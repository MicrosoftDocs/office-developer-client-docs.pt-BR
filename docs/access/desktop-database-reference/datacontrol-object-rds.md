---
title: Objeto DataControl (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ffe674f3aa02e5cc8b1f89375ca66b4efa623f2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709779"
---
# <a name="datacontrol-object-rds"></a><span data-ttu-id="cbee2-102">Objeto DataControl (RDS)</span><span class="sxs-lookup"><span data-stu-id="cbee2-102">DataControl object (RDS)</span></span>

<span data-ttu-id="cbee2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbee2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbee2-104">Vincula uma consulta de dados do [Recordset](recordset-object-ado.md) a um ou mais controles (por exemplo, uma caixa de texto, o controle de grade ou uma caixa de combinação) para exibir os dados do **Recordset** em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="cbee2-104">Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbee2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbee2-105">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="cbee2-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbee2-106">Remarks</span></span>

<span data-ttu-id="cbee2-107">A ID de classe do objeto **RDS.DataControl** é BD96C556-65A3-11D0-983A-00C04FC29E33.</span><span class="sxs-lookup"><span data-stu-id="cbee2-107">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="cbee2-p101">[!OBSERVAçãO] Se você receber um erro informando que um objeto [RDS.DataSpace](dataspace-object-rds.md) ou **RDS.DataControl** não foi carregado, verifique se está usando a ID de classe correta. As IDs de classe desses objetos foram alteradas da versão 1.0 e 1.1.</span><span class="sxs-lookup"><span data-stu-id="cbee2-p101">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID. The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="cbee2-110">Para um cenário básico, é necessário definir somente as propriedades **SQL**, **Connect** e **Server** do objeto **RDS.DataControl**, que chamará automaticamente o objeto corporativo padrão, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="cbee2-110">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="cbee2-111">Todas as propriedades do **RDS.DataControl** são opcionais porque os objetos corporativos personalizados podem substituir sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="cbee2-111">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="cbee2-112">[!OBSERVAçãO] Se você consultar vários resultados, somente o primeiro [Recordset](recordset-object-ado.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="cbee2-112">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="cbee2-113">Se forem necessárias várias definições de resultados, atribua cada uma ao próprio **DataControl**.</span><span class="sxs-lookup"><span data-stu-id="cbee2-113">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="cbee2-114">Um exemplo de uma consulta de vários resultados poderia ser o seguinte: `"Select * from Authors, Select * from Topics"`.</span><span class="sxs-lookup"><span data-stu-id="cbee2-114">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="cbee2-p103">A adição de "DFMode=20;" à sua sequência de conexão durante o uso do objeto **RDS.DataControl** pode melhorar o desempenho do servidor na atualização de dados. Com essa definição, o objeto **RDSServer.DataFactory** do servidor usa um modo de recursos menos intensivo. No entanto, os seguintes recursos não estão disponíveis nesta configuração:</span><span class="sxs-lookup"><span data-stu-id="cbee2-p103">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data. With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode. However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="cbee2-118">Uso de consultas parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="cbee2-118">Using parameterized queries.</span></span>

  - <span data-ttu-id="cbee2-119">Obtenção de informações de parâmetro ou de coluna antes da chamada do método **Execute**.</span><span class="sxs-lookup"><span data-stu-id="cbee2-119">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="cbee2-120">Definição de **Transacionar Atualizações** como **Verdadeira**.</span><span class="sxs-lookup"><span data-stu-id="cbee2-120">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="cbee2-121">Obtenção de status da linha.</span><span class="sxs-lookup"><span data-stu-id="cbee2-121">Getting row status.</span></span>

  - <span data-ttu-id="cbee2-122">Chamada do método [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cbee2-122">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="cbee2-123">Atualização (de forma explícita ou automática) por meio da propriedade [Update Resync](update-resync-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cbee2-123">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="cbee2-124">Definição das propriedades **Command** ou [Recordset](recordset-sourcerecordset-properties-rds.md).</span><span class="sxs-lookup"><span data-stu-id="cbee2-124">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="cbee2-125">Uso de **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="cbee2-125">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="cbee2-p104">O objeto **RDS.DataControl** é executado no modo assíncronopor padrão. Se você solicitar a execução síncrona do aplicativo, defina o parâmetro [ExecuteOptions](executeoptions-property-rds.md) igual a **adcExecSync** e o parâmetro [FetchOptions](fetchoptions-property-rds.md) igual a **adcFetchUpFront**, como mostra o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="cbee2-p104">The **RDS.DataControl** object runs in asynchronous mode by default. If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

<span data-ttu-id="cbee2-p105">Use um objeto **RDS.DataControl** para vincular os resultados de uma única consulta a um ou vários controles visuais. Por exemplo, suponha que você codificou uma consulta solicitando dados do cliente, como Nome, Residência, Local de Nascimento, Idade e Status de Prioridade. Use um único objeto **RDS.DataControl** para exibir o Nome, a Idade e a Região do cliente em três caixas de texto separadas; o Status de Prioridade do Cliente em uma caixa de seleção e todos os dados em um controle de grade.</span><span class="sxs-lookup"><span data-stu-id="cbee2-p105">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls. For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status. You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="cbee2-p106">Use objetos **RDS.DataControl** diferentes para vincular resultados de várias consultas a controles visuais diferentes. Por exemplo, suponha que você está usando uma consulta para obter informações sobre um cliente e uma segunda consulta para obter informações da mercadoria comprada pelo cliente. Você deseja exibir resultados da primeira consulta em três caixas de texto e uma caixa de seleção e os resultados da segunda consulta em um controle de grade. Se você usar o objeto corporativo padrão (**RDSServer.DataFactory**), será necessário fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cbee2-p106">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls. For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased. You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control. If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

  - <span data-ttu-id="cbee2-135">Adicionar dois **RDS. DataControl** objetos para sua página da Web.</span><span class="sxs-lookup"><span data-stu-id="cbee2-135">Add two **RDS.DataControl** objects to your webpage.</span></span>

  - <span data-ttu-id="cbee2-p107">Gravar duas consultas, uma para cada propriedade **SQL** de dois objetos **RDS.DataControl**. O primeiro objeto **RDS.DataControl** conterá uma consulta SQL solicitando informações do cliente; o segundo conterá uma consulta solicitando uma lista de mercadorias compradas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="cbee2-p107">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects. One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="cbee2-138">Em cada uma das marcas OBJECT dos controles vinculados, especifique o valor DATAFLD para definir os valores dos dados que você deseja exibir em cada controle visual.</span><span class="sxs-lookup"><span data-stu-id="cbee2-138">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="cbee2-139">Não há nenhuma restrição de contagem no número de **RDS. DataControl** objetos que você pode inserir por meio de marcas OBJECT em uma única página da Web.</span><span class="sxs-lookup"><span data-stu-id="cbee2-139">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="cbee2-140">Quando você define o **RDS. DataControl** do objeto em uma página da Web, use valores **Height** e **Width** diferentes de zero como 1 (para evitar a inclusão de espaços adicionais).</span><span class="sxs-lookup"><span data-stu-id="cbee2-140">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>

<span data-ttu-id="cbee2-141">Os componentes do cliente RDS já foram incluídos como parte do Internet Explorer 4.0; por esse motivo, não é necessário incluir um parâmetro CODEBASE na marca de objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="cbee2-141">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="cbee2-142">Com o Internet Explorer 4.0 ou posterior, você pode vincular a dados usando os controles HTML e controles ActiveX somente se estes estiverem marcados como controles de modelo apartment.</span><span class="sxs-lookup"><span data-stu-id="cbee2-142">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="cbee2-143">**Usuários do Microsoft Visual Basic** O RDS. \*\* DataControl\*\* só é usada em aplicativos baseados na web.</span><span class="sxs-lookup"><span data-stu-id="cbee2-143">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="cbee2-144">Não é necessário um aplicativo cliente do Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cbee2-144">A Visual Basic client application has no need for it.</span></span>

