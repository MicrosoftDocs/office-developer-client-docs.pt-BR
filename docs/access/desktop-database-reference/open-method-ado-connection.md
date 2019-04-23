---
title: Método Open (Connection do ADO)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288424"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="022b6-102">Método Open (Connection do ADO)</span><span class="sxs-lookup"><span data-stu-id="022b6-102">Open method (ADO Connection)</span></span>

<span data-ttu-id="022b6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="022b6-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="022b6-104">Abre uma conexão a uma fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="022b6-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="022b6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="022b6-105">Syntax</span></span>

<span data-ttu-id="022b6-106">*conexão*. *ConnectionString*aberta, *userid*, *senha*, *Opções*</span><span class="sxs-lookup"><span data-stu-id="022b6-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="022b6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="022b6-107">Parameters</span></span>

|<span data-ttu-id="022b6-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="022b6-108">Parameter</span></span>|<span data-ttu-id="022b6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="022b6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="022b6-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="022b6-110">*ConnectionString*</span></span> |<span data-ttu-id="022b6-p101">Opcional. Um valor **String** que contém informações de conexão. Consulte a propriedade [ConnectionString](connectionstring-property-ado.md) para obter detalhes sobre definições válidas.</span><span class="sxs-lookup"><span data-stu-id="022b6-p101">Optional. A **String** value that contains connection information. See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>|
|<span data-ttu-id="022b6-114">*UserID*</span><span class="sxs-lookup"><span data-stu-id="022b6-114">*UserID*</span></span> |<span data-ttu-id="022b6-p102">Opcional. Um valor **String** que contém um nome de usuário que será utilizado ao estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="022b6-p102">Optional. A **String** value that contains a user name to use when establishing the connection.</span></span>|
|<span data-ttu-id="022b6-117">*Password*</span><span class="sxs-lookup"><span data-stu-id="022b6-117">*Password*</span></span> |<span data-ttu-id="022b6-p103">Opcional. Um valor **String** que contém uma senha que será utilizada ao estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="022b6-p103">Optional. A **String** value that contains a password to use when establishing the connection.</span></span>|
|<span data-ttu-id="022b6-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="022b6-120">*Options*</span></span> |<span data-ttu-id="022b6-p104">Opcional. Um valor [ConnectOptionEnum](connectoptionenum.md) que determina se esse método deve retornar depois (sincronamente) ou antes (assincronamente) de a conexão ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="022b6-p104">Optional. A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>|

## <a name="remarks"></a><span data-ttu-id="022b6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="022b6-123">Remarks</span></span>

<span data-ttu-id="022b6-p105">A utilização do método **Open** em um objeto [Connection](connection-object-ado.md) estabelece a conexão física a uma fonte de dados. Depois da conclusão com êxito desse método, a conexão estará ativa e será possível emitir comandos com relação à mesma e processar os resultados.</span><span class="sxs-lookup"><span data-stu-id="022b6-p105">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source. After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="022b6-126">Use o argumento *ConnectionString* opcional para especificar uma cadeia de caracteres de conexão contendo uma série de instruções *Argument* *= Value* separadas por ponto-e-vírgula ou um recurso de arquivo ou diretório identificado com uma URL.</span><span class="sxs-lookup"><span data-stu-id="022b6-126">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="022b6-127">A propriedade **ConnectionString** herda automaticamente o valor utilizado para o argumento *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="022b6-127">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="022b6-128">Portanto, é possível definir a propriedade **ConnectionString** do objeto **Connection** antes de abri-lo ou utilizar o argumento *ConnectionString* para definir ou substituir os parâmetros da conexão atual durante a chamada ao método **Open**.</span><span class="sxs-lookup"><span data-stu-id="022b6-128">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="022b6-129">Se você passar informações de usuário e senha no argumento *ConnectionString* e nos argumentos opcionais *UserID* e *Password*, os argumentos *UserID* e *Password* substituirão os valores especificados em *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="022b6-129">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="022b6-p107">Quando concluir as operações em um **Connection** aberto, utilize o método [Close](close-method-ado.md) para liberar quaisquer recursos associados do sistema. O fechamento de um objeto não o remove da memória; é possível alterar as definições de propriedade e utilizar o método **Open** para abri-lo novamente mais tarde. Para eliminar completamente um objeto da memória, defina a variável do objeto como *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="022b6-p107">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources. Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later. To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="022b6-133">**Uso do Remote Data Service** Quando usado em um objeto **Connection** do lado do cliente, o método **Open** não estabelece realmente uma conexão com o servidor até que um [Recordset](recordset-object-ado.md) seja aberto no objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="022b6-133">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="022b6-134">[!OBSERVAçãO] URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="022b6-134">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="022b6-135">Para obter mais informações, consulte [URLs absolutas e relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="022b6-135">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


