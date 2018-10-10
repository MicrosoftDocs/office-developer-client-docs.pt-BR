---
title: Propriedade ActiveConnection (ADO)
TOCTitle: ActiveConnection Property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d44a17d192abdb68755a2010184b4fb4d6531174
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465391"
---
# <a name="activeconnection-property-ado"></a><span data-ttu-id="ad1cc-102">Propriedade ActiveConnection (ADO)</span><span class="sxs-lookup"><span data-stu-id="ad1cc-102">ActiveConnection Property (ADO)</span></span>


<span data-ttu-id="ad1cc-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad1cc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ad1cc-104">Indica a qual objeto [Connection](connection-object-ado.md) pertence o objeto [Command](command-object-ado.md), [Recordset](recordset-object-ado.md) ou [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ad1cc-104">Indicates to which [Connection](connection-object-ado.md) object the specified [Command](command-object-ado.md), [Recordset](recordset-object-ado.md), or [Record](record-object-ado.md) object currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ad1cc-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ad1cc-105">Settings and Return Values</span></span>

<span data-ttu-id="ad1cc-p101">Configura ou retorna um valor **String** contendo uma definição para uma conexão, caso a conexão esteja fechada, ou um **Variant** contendo o objeto **Connection** atual no caso de a conexão estar aberta. O padrão é uma referência nula ao objeto. Consulte também a propriedade [ConnectionString](connectionstring-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ad1cc-p101">Sets or returns a **String** value that contains a definition for a connection if the connection is closed, or a **Variant** containing the current **Connection** object if the connection is open. Default is a null object reference. See the [ConnectionString](connectionstring-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad1cc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad1cc-109">Remarks</span></span>

<span data-ttu-id="ad1cc-110">Use a propriedade **ActiveConnection** para determinar o objeto **Connection** no qual o objeto **Command** especificado será executado ou o objeto **Recordset** especificado será aberto.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-110">Use the **ActiveConnection** property to determine the **Connection** object over which the specified **Command** object will execute or the specified **Recordset** will be opened.</span></span>

<span data-ttu-id="ad1cc-111">**Command**</span><span class="sxs-lookup"><span data-stu-id="ad1cc-111">**Command**</span></span>

<span data-ttu-id="ad1cc-112">Para os objetos **Command**, a propriedade **ActiveConnection** é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-112">For **Command** objects, the **ActiveConnection** property is read/write.</span></span>

<span data-ttu-id="ad1cc-113">Ocorrerá um erro se você tentar chamar o método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) em um objeto **Command** antes de configurar essa propriedade como um objeto **Connection** aberto ou uma sequência de conexão válida.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-113">If you attempt to call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method on a **Command** object before setting this property to an open **Connection** object or valid connection string, an error occurs.</span></span>

<span data-ttu-id="ad1cc-114">**Microsoft Visual Basic** Configurar a propriedade **ActiveConnection** como *Nothing* desassocia o objeto **Command** da **Conexão** atual e faz com que o provedor liberar quaisquer recursos associados na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-114">**Microsoft Visual Basic**Setting the **ActiveConnection** property to *Nothing* disassociates the **Command** object from the current **Connection** and causes the provider to release any associated resources on the data source.</span></span> <span data-ttu-id="ad1cc-115">Assim, você pode associar o objeto **Command** ao mesmo objeto **Connection** ou a um outro.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-115">You can then associate the **Command** object with the same or another **Connection** object.</span></span> <span data-ttu-id="ad1cc-116">Alguns provedores permitem que você altere a configuração da propriedade de uma **Conexão** para outra, sem precisar primeiro definir a propriedade como *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-116">Some providers allow you to change the property setting from one **Connection** to another, without having to first set the property to *Nothing*.</span></span>

<span data-ttu-id="ad1cc-117">Se a coleção [Parameters](parameters-collection-ado.md) do objeto **Command** contiver parâmetros fornecidos pelo provedor, a coleção está desmarcada, se você definir a propriedade **ActiveConnection** como *Nothing* ou para outro objeto de **Conexão** .</span><span class="sxs-lookup"><span data-stu-id="ad1cc-117">If the [Parameters](parameters-collection-ado.md) collection of the **Command** object contains parameters supplied by the provider, the collection is cleared if you set the **ActiveConnection** property to *Nothing* or to another **Connection** object.</span></span> <span data-ttu-id="ad1cc-118">Se você cria objetos [Parameter](parameter-object-ado.md) e usá-los para preencher a coleção **Parameters** do objeto **Command** manualmente, definindo o **ActiveConnection** como *Nothing* ou para outro objeto de **Conexão** de propriedade deixa a coleção **Parameters** intacta.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-118">If you manually create [Parameter](parameter-object-ado.md) objects and use them to fill the **Parameters** collection of the **Command** object, setting the **ActiveConnection** property to *Nothing* or to another **Connection** object leaves the **Parameters** collection intact.</span></span>

<span data-ttu-id="ad1cc-p104">O fechamento de um objeto **Connection** ao qual um objeto **Command** está associado define a propriedade **ActiveConnection** como *Nothing*. A definição dessa propriedade para um objeto **Connection** fechado gera um erro.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-p104">Closing the **Connection** object with which a **Command** object is associated sets the **ActiveConnection** property to *Nothing*. Setting this property to a closed **Connection** object generates an error.</span></span>

<span data-ttu-id="ad1cc-121">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="ad1cc-121">**Recordset**</span></span>

<span data-ttu-id="ad1cc-p105">Para objetos **Recordset** abertos ou para objetos **Recordset** cuja propriedade [Source](source-property-ado-recordset.md) esteja definida como um objeto **Command** válido, a propriedade **ActiveConnection** é somente leitura. Caso contrário, ela é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-p105">For open **Recordset** objects or for **Recordset** objects whose [Source](source-property-ado-recordset.md) property is set to a valid **Command** object, the **ActiveConnection** property is read-only. Otherwise, it is read/write.</span></span>

<span data-ttu-id="ad1cc-p106">Você pode definir essa propriedade como um objeto **Connection** válido ou como uma sequência de conexão válida. Neste caso, o provedor cria um novo objeto **Connection** usando essa definição e abre a conexão. Além disso, o provedor pode definir essa propriedade para o novo objeto **Connection** de modo que você acesse o objeto **Connection** para obter informações de erro estendidas ou execute outros comandos.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-p106">You can set this property to a valid **Connection** object or to a valid connection string. In this case, the provider creates a new **Connection** object using this definition and opens the connection. Additionally, the provider may set this property to the new **Connection** object to give you a way to access the **Connection** object for extended error information or to execute other commands.</span></span>

<span data-ttu-id="ad1cc-127">Se você usar o argumento *ActiveConnection* do método [Open](open-method-ado-recordset.md) para abrir um objeto **Recordset** , a propriedade **ActiveConnection** herdará o valor do argumento.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-127">If you use the *ActiveConnection* argument of the [Open](open-method-ado-recordset.md) method to open a **Recordset** object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="ad1cc-128">Se você configurar a propriedade **Source** do objeto **Recordset** como uma variável de objeto **Command** válida, a propriedade **ActiveConnection** do **Recordset** herdará a definição da propriedade **ActiveConnection** do objeto **Command**.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-128">If you set the **Source** property of the **Recordset** object to a valid **Command** object variable, the **ActiveConnection** property of the **Recordset** inherits the setting of the **Command** object's **ActiveConnection** property.</span></span>

<span data-ttu-id="ad1cc-129">**Uso de serviço de dados remotos** Quando usado em um objeto Recordset do lado do cliente, essa propriedade pode ser definida apenas como uma sequência de conexão ou (no Microsoft Visual Basic ou Visual Basic, Scripting Edition) como *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-129">**Remote Data Service Usage**When used on a client-side Recordset object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to *Nothing*.</span></span>

<span data-ttu-id="ad1cc-130">**Record**</span><span class="sxs-lookup"><span data-stu-id="ad1cc-130">**Record**</span></span>

<span data-ttu-id="ad1cc-p107">Essa propriedade é leitura/gravação quando o objeto **Record** estiver fechado, podendo conter uma sequência de conexão ou referência a um objeto **Connection** aberto. Ela é somente leitura quando o objeto **Record** estiver aberto e contiver uma referência a um objeto **Connection** aberto.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-p107">This property is read/write when the **Record** object is closed, and may contain a connection string or reference to an open **Connection** object. This property is read-only when the **Record** object is open, and contains a reference to an open **Connection** object.</span></span>

<span data-ttu-id="ad1cc-p108">Um objeto **Connection** é criado implicitamente quando o objeto **Record** é aberto a partir de uma URL. Abra o **Record** com um objeto **Connection** existente e aberto atribuindo o objeto **Connection** a essa propriedade ou usando o objeto **Connection** como um parâmetro na chamada do método [Open](open-method-ado-record.md). Se o **Record** for aberto a partir de um **Record** ou [Recordset](recordset-object-ado.md) existente, ele será automaticamente associado ao objeto **Connection** do objeto **Record** ou **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-p108">A **Connection** object is created implicitly when the **Record** object is opened from a URL. Open the **Record** with an existing, open **Connection** object by assigning the **Connection** object to this property, or using the **Connection** object as a parameter in the [Open](open-method-ado-record.md) method call. If the **Record** is opened from an existing **Record** or [Recordset](recordset-object-ado.md), then it is automatically associated with that **Record** or **Recordset** object's **Connection** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ad1cc-p109">[!OBSERVAçãO] As URLs que usam o esquema http invocarão automaticamente o <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. Para obter mais informações, consulte <A href="absolute-and-relative-urls.md">URLs absolutas e relativas</A>.</span><span class="sxs-lookup"><span data-stu-id="ad1cc-p109">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


