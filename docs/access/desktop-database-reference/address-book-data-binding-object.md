---
title: Objeto de vinculação de dados do catálogo de endereços
TOCTitle: Address Book Data-Binding Object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfa95c05ac87648c4d69e3d781614d9cd553bc02
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464151"
---
# <a name="address-book-data-binding-object"></a><span data-ttu-id="6c6e9-102">Objeto de vinculação de dados do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="6c6e9-102">Address Book Data-Binding Object</span></span>


<span data-ttu-id="6c6e9-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c6e9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6c6e9-p101">O aplicativo do catálogo de endereços usa o objeto [RDS.DataControl](datacontrol-object-rds.md) para vincular os dados do banco de dados SQL Server para um objeto visual (nesse caso, uma tabela DHTML) na página HTML do cliente de aplicativos. A lógica do programa VBScript controlada por eventos usa o [RDS.DataControl](datacontrol-object-rds.md) para:</span><span class="sxs-lookup"><span data-stu-id="6c6e9-p101">The Address Book application uses the [RDS.DataControl](datacontrol-object-rds.md) object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page. The event-driven VBScript program logic uses the [RDS.DataControl](datacontrol-object-rds.md) to:</span></span>

  - <span data-ttu-id="6c6e9-106">Consultar o banco de dados, enviar atualizações ao banco de dados e atualizar a grade de dados.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-106">Query the database, send updates to the database, and refresh the data grid.</span></span>

  - <span data-ttu-id="6c6e9-107">Permite que os usuários se movimentem para o primeiro, próximo, anterior ou último registro na grade de dados.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-107">Allow users to move to the first, next, previous, or last record in the data grid.</span></span>

<span data-ttu-id="6c6e9-108">O seguinte código define o componente **RDS.DataControl**:</span><span class="sxs-lookup"><span data-stu-id="6c6e9-108">The following code defines the **RDS.DataControl** component:</span></span>

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

<span data-ttu-id="6c6e9-p102">A marca OBJECT define o componente **RDS.DataControl** no programa. A marca inclui dois tipos de parâmetros:</span><span class="sxs-lookup"><span data-stu-id="6c6e9-p102">The OBJECT tag defines the **RDS.DataControl** component in the program. The tag includes two types of parameters:</span></span>

  - <span data-ttu-id="6c6e9-111">Os associados à marca OBJECT genérica.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-111">Those associated with the generic OBJECT tag.</span></span>

  - <span data-ttu-id="6c6e9-112">Os específicos ao objeto **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-112">Those specific to the **RDS.DataControl** object.</span></span>

## <a name="generic-object-tag-parameters"></a><span data-ttu-id="6c6e9-113">Parâmetros da marca OBJECT genérica</span><span class="sxs-lookup"><span data-stu-id="6c6e9-113">Generic OBJECT Tag Parameters</span></span>

<span data-ttu-id="6c6e9-114">A tabela a seguir descreve os parâmetros associados à marca OBJECT.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-114">The following table describes the parameters associated with the OBJECT tag.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c6e9-115">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c6e9-115">Parameter</span></span></p></th>
<th><p><span data-ttu-id="6c6e9-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c6e9-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c6e9-117"><strong><em>CLASSID</em></strong></span><span class="sxs-lookup"><span data-stu-id="6c6e9-117"><strong><em>CLASSID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="6c6e9-p103">Um número exclusivo de 128 bits que identifica o tipo de objeto incorporado ao sistema. Esse identificador é mantido no registro de sistema do computador local. (Para os IDs de classe do objeto <strong>RDS.DataControl</strong>, consulte o <a href="datacontrol-object-rds.md">Objeto RDS.DataControl</a>.)</span><span class="sxs-lookup"><span data-stu-id="6c6e9-p103">A unique, 128-bit number that identifies the type of embedded object to the system. This identifier is maintained in the local computer's system registry. (For the class IDs of the <strong>RDS.DataControl</strong> object, see <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c6e9-121"><strong><em>ID</em></strong></span><span class="sxs-lookup"><span data-stu-id="6c6e9-121"><strong><em>ID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="6c6e9-122">Define um identificador que abrange o documento para o objeto incorporado que é usado para identificá-lo no código.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-122">Defines a document-wide identifier for the embedded object that is used to identify it in code.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a><span data-ttu-id="6c6e9-123">Parâmetros da marca RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="6c6e9-123">RDS.DataControl Tag Parameters</span></span>

<span data-ttu-id="6c6e9-p104">A tabela a seguir descreve os parâmetros específicos ao objeto **RDS.DataControl**. (Para obter uma lista completa de parâmetros de objetos **RDS.DataControl** e ao implementá-los, consulte o [objeto RDS.DataControl](datacontrol-object-rds.md).)</span><span class="sxs-lookup"><span data-stu-id="6c6e9-p104">The following table describes the parameters specific to the **RDS.DataControl** object. (For a complete list of the **RDS.DataControl** object parameters, and when to implement them, see [RDS.DataControl object](datacontrol-object-rds.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c6e9-126">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c6e9-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="6c6e9-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c6e9-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c6e9-128"><a href="server-property-rds.md">SERVIDOR</a></span><span class="sxs-lookup"><span data-stu-id="6c6e9-128"><a href="server-property-rds.md">SERVER</a></span></span></p></td>
<td><p><span data-ttu-id="6c6e9-129">Se você estiver usando o HTTP, o valor é o nome do computador servidor precedido por https://.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-129">If you are using HTTP, the value is the name of the server computer preceded by https:// .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c6e9-130"><a href="connect-property-rds.md">CONECTE-SE</a></span><span class="sxs-lookup"><span data-stu-id="6c6e9-130"><a href="connect-property-rds.md">CONNECT</a></span></span></p></td>
<td><p><span data-ttu-id="6c6e9-131">Fornece informações de conexão necessárias para que o <strong>RDS.DataControl</strong> se conecte ao SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-131">Provides the necessary connection information for the <strong>RDS.DataControl</strong> to connect to SQL Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c6e9-132"><a href="https://msdn.microsoft.com/library/jj248989(v=office.15)">SQL</a></span><span class="sxs-lookup"><span data-stu-id="6c6e9-132"><a href="https://msdn.microsoft.com/library/jj248989(v=office.15)">SQL</a></span></span></p></td>
<td><p><span data-ttu-id="6c6e9-133">Define ou retorna a cadeia de consulta usada para recuperar o <a href="recordset-object-ado.md">Recordset</a>.</span><span class="sxs-lookup"><span data-stu-id="6c6e9-133">Sets or returns the query string used to retrieve the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
</tbody>
</table>

