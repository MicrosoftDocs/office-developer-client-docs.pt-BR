---
title: Propriedade ActiveConnection (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 372dac11500647af75881ae6b4aee22a391a32c9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703185"
---
# <a name="activeconnection-property-ado-md"></a><span data-ttu-id="6e01b-102">Propriedade ActiveConnection (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="6e01b-102">ActiveConnection property (ADO MD)</span></span>

<span data-ttu-id="6e01b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e01b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e01b-104">Indica a que objeto [Connection](connection-object-ado.md) do ADO pertence o conjunto de células ou o catálogo atual.</span><span class="sxs-lookup"><span data-stu-id="6e01b-104">Indicates to which ADO [Connection](connection-object-ado.md) object the current cellset or catalog currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6e01b-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6e01b-105">Settings and return values</span></span>

<span data-ttu-id="6e01b-p101">Define ou retorna um objeto **Variant** que contém uma cadeia de caracteres que define uma conexão ou um objeto **Connection**. O padrão é vazio.</span><span class="sxs-lookup"><span data-stu-id="6e01b-p101">Sets or returns a **Variant** that contains a string defining a connection or **Connection** object. The default is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e01b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e01b-108">Remarks</span></span>

<span data-ttu-id="6e01b-p102">Você pode definir esta propriedade como um objeto **Connection** válido do ADO ou como um cadeia de caracteres de conexão válida. Quando essa propriedade é definida como uma cadeia de caracteres de conexão, o provedor cria um novo objeto **Connection** usando essa definição e abre a conexão.</span><span class="sxs-lookup"><span data-stu-id="6e01b-p102">You can set this property to a valid ADO **Connection** object or to a valid connection string. When this property is set to a connection string, the provider creates a new **Connection** object using this definition and opens the connection.</span></span>

<span data-ttu-id="6e01b-111">Se você usar o argumento **ActiveConnection** do método [Open](open-method-ado-md.md) para abrir um objeto [Cellset](cellset-object-ado-md.md), a propriedade **ActiveConnection** herdará o valor do argumento.</span><span class="sxs-lookup"><span data-stu-id="6e01b-111">If you use the **ActiveConnection** argument of the [Open](open-method-ado-md.md) method to open a [Cellset](cellset-object-ado-md.md) object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="6e01b-p103">A definição da propriedade **ActiveConnection** de um objeto [Catalog](catalog-object-ado-md.md) como **Nothing** libera os dados associados, incluindo os dados da coleção [CubeDefs](cubedefs-collection-ado-md.md) e os objetos [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) e [Member](member-object-ado-md.md) relacionados. O fechamento do objeto **Connection** usado para abrir um **Catalog** tem o mesmo efeito que a definição da propriedade **ActiveConnection** como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="6e01b-p103">Setting the **ActiveConnection** property of a [Catalog](catalog-object-ado-md.md) object to **Nothing** releases the associated data, including data in the [CubeDefs](cubedefs-collection-ado-md.md) collection and any related [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md) objects. Closing a **Connection** object that was used to open a **Catalog** has the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

<span data-ttu-id="6e01b-114">A alteração do banco de dados padrão da conexão referenciada pela propriedade **ActiveConnection** de um objeto **Catalog** invalida o conteúdo do **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="6e01b-114">Changing the default database of the connection referenced by the **ActiveConnection** property of a **Catalog** object invalidates the contents of the **Catalog**.</span></span>

<span data-ttu-id="6e01b-115">Ocorrerá um erro se você tentar alterar a propriedade **ActiveConnection** de um objeto **Cellset** aberto.</span><span class="sxs-lookup"><span data-stu-id="6e01b-115">An error will occur if you attempt to change the **ActiveConnection** property for an open **Cellset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="6e01b-p104">[!OBSERVAçãO] No Visual Basic, lembre-se de usar a palavra-chave **Set** ao definir a propriedade **ActiveConnection** como um objeto **Connection**. Se você omitir a palavra-chave **Set**, estará realmente definindo a propriedade **ActiveConnection** de forma equivalente à propriedade padrão do objeto **Connection**, **ConnectionString**. O código funcionará; contudo, você criará uma conexão adicional à fonte de dados, que poderá ter implicações de desempenho negativas.</span><span class="sxs-lookup"><span data-stu-id="6e01b-p104">In Visual Basic, remember to use the **Set** keyword when setting the **ActiveConnection** property to a **Connection** object. If you omit the **Set** keyword, you will actually be setting the **ActiveConnection** property equal to the **Connection** object's default property, **ConnectionString**. The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</span></span>

<span data-ttu-id="6e01b-p105">Ao usar o provedor de dados MSOLAP, defina a fonte de dados em uma cadeia de caracteres de conexão como o nome de um servidor e defina o catálogo inicial como o nome de um catálogo da fonte de dados. Para se conectar a um arquivo de cubo que esteja desconectado de um servidor, defina o local como o caminho completo para o arquivo .CUB. Nesse caso, defina o provedor com o respectivo nome. Por exemplo, a cadeia de caracteres a seguir conecta-se a um catálogo chamado Bobs Video Store em um servidor chamado Servername com o Provedor MSOLAP:</span><span class="sxs-lookup"><span data-stu-id="6e01b-p105">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source. To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file. In either case, set the provider to the provider name. For example, the following string connects to a catalog named Bobs Video Store on a server named Servername with the MSOLAP Provider:</span></span>

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

<span data-ttu-id="6e01b-123">A sequência a seguir conecta a um arquivo de cubo local no local c:\\MSDASDK\\amostras\\oledb\\olap\\dados\\bobsvid.cub:</span><span class="sxs-lookup"><span data-stu-id="6e01b-123">The following string connects to a local cube file at the location C:\\MSDASDK\\samples\\oledb\\olap\\data\\bobsvid.cub:</span></span>

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

