---
title: Objeto Command (ADO)
TOCTitle: Command Object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 153f59ebbcfae89f6358fe0d707791aab8a8cdd7
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864071"
---
# <a name="command-object-ado"></a><span data-ttu-id="b038e-102">Objeto Command (ADO)</span><span class="sxs-lookup"><span data-stu-id="b038e-102">Command Object (ADO)</span></span>


<span data-ttu-id="b038e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b038e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b038e-104">Define um comando específico que você pretende executar em relação a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="b038e-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="b038e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b038e-105">Remarks</span></span>

<span data-ttu-id="b038e-p101">Use um objeto **Command** para consultar um banco de dados e retornar registros em um objeto [Recordset](recordset-object-ado.md), para executar uma operação em massa ou manipular a estrutura de um banco de dados. Dependendo da funcionalidade do provedor, alguns métodos e algumas coleções e propriedades **Command** poderão gerar um erro quando mencionados.</span><span class="sxs-lookup"><span data-stu-id="b038e-p101">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database. Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="b038e-108">Com as coleções, os métodos e as propriedades de um objeto **Command**, você pode fazer o que segue:</span><span class="sxs-lookup"><span data-stu-id="b038e-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="b038e-109">Definir o texto executável do comando (por exemplo, uma instrução SQL) com a propriedade [CommandText](commandtext-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b038e-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="b038e-110">Definir consultas com parâmetros ou argumentos de procedimentos armazenados usando objetos [Parameter](parameter-object-ado.md) e a coleção [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b038e-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="b038e-111"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b038e-111"><<<<<<< HEAD</span></span>
  - <span data-ttu-id="b038e-112">Executar um comando e retornar um objeto **Recordset**, se for adequado, com o método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b038e-112">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>
=======
  - <span data-ttu-id="b038e-113">Executar um comando e retornar um objeto **Recordset**, se for adequado, com o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).</span><span class="sxs-lookup"><span data-stu-id="b038e-113">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>
>>>>>>> <span data-ttu-id="b038e-114">mestre</span><span class="sxs-lookup"><span data-stu-id="b038e-114">master</span></span>

  - <span data-ttu-id="b038e-115">Especificar o tipo de comando com a propriedade [CommandType](commandtype-property-ado.md) antes da execução para otimizar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="b038e-115">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="b038e-116">Controlar se o provedor salvará uma versão preparada (ou compilada) do comando antes da execução com a propriedade [Prepared](prepared-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b038e-116">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="b038e-117">Definir o número de segundos que um provedor aguardará um comando para executar a propriedade [CommandTimeout](commandtimeout-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b038e-117">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="b038e-118">Associar uma conexão aberta com um objeto **Command** definindo sua propriedade [ActiveConnection](activeconnection-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b038e-118">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="b038e-119">Definir a propriedade [Name](name-property-ado.md) para identificar o objeto **Command** como um método no objeto [Connection](connection-object-ado.md) associado.</span><span class="sxs-lookup"><span data-stu-id="b038e-119">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="b038e-120">Passar um objeto **Command** para a propriedade [Source](source-property-ado-recordset.md) de um **Recordset** para obter dados.</span><span class="sxs-lookup"><span data-stu-id="b038e-120">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="b038e-121">Acessar os atributos específicos do provedor com a coleção [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b038e-121">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

> [!NOTE]
> <span data-ttu-id="b038e-p102">[!OBSERVAçãO] Para executar uma consulta sem usar um objeto **Command**, passe uma sequência de consulta para o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) de um objeto **Connection** ou para o método [Open](open-method-ado-recordset.md) de um objeto **Recordset**. No entanto, um objeto **Command** será necessário quando você quiser insistircom o texto de comando e reexecutá-lo ou usar os parâmetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="b038e-p102">To execute a query without using a **Command** object, pass a query string to the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method of a **Connection** object or to the [Open](open-method-ado-recordset.md) method of a **Recordset** object. However, a **Command** object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

<span data-ttu-id="b038e-p103">Para criar um objeto **Command**, de forma independente, de um objeto **Connection** definido anteriormente, defina a propriedade **ActiveConnection** como uma sequência de conexão válida. O ADO ainda criará um objeto **Connection**, mas não atribuirá esse objeto a uma variável de objeto. No entanto, se você estiver associando vários objetos **Command** com a mesma conexão, deverá criar e abrir, de forma explícita, um objeto **Connection**; isso atribui o objeto **Connection** a uma variável de objeto. Se você não definir a propriedade **ActiveConnection** do objeto **Command** para esta variável de objeto, o ADO criará um novo objeto **Connection** para cada objeto **Command**, mesmo se você usar a mesma sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="b038e-p103">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string. ADO still creates a **Connection** object, but it doesn't assign that object to an object variable. However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable. If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="b038e-p104">Para executar um objeto **Command**, basta chamá-lo por meio da propriedade [Name](name-property-ado.md) do objeto **Connection** associado. **Command** deve ter a propriedade **ActiveConnection** definida como o objeto **Connection**. Se **Command** tiver parâmetros, passe seus valores como argumentos para o método.</span><span class="sxs-lookup"><span data-stu-id="b038e-p104">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object. The **Command** must have its **ActiveConnection** property set to the **Connection** object. If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="b038e-p105">Se dois ou mais objetos **Command** forem executados na mesma conexão e o objeto **Command** estiver em um procedimento armazenado com parâmetros de saída, ocorrerá um erro. Para executar cada objeto **Command**, use conexões separadas ou desconecte todos os outros objetos **Command** da conexão.</span><span class="sxs-lookup"><span data-stu-id="b038e-p105">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs. To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="b038e-p106">A coleção **Parameters** é o membro padrão do objeto **Command**. Como resultado, as duas instruções de código a seguir são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b038e-p106">The **Parameters** collection is the default member of the **Command** object. As a result, the following two code statements are equivalent.</span></span>

