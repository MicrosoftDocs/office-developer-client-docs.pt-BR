---
<span data-ttu-id="c138a-101"><<<<<<< Título cabeça: propriedade CursorLocation (ADO) TOCTitle: propriedade CursorLocation (ADO) === título: propriedade CursorLocation (ADO) TOCTitle: propriedade CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="c138a-101"><<<<<<< HEAD title: CursorLocation Property (ADO) TOCTitle: CursorLocation Property (ADO) ======= title: CursorLocation property (ADO) TOCTitle: CursorLocation property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c138a-102">ms:assetid de mestre: 8a048bd4-ae25-a555-1c07-14364b7e6560 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15) ms:contentKeyID: ms.date 48546182: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="c138a-102">master ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15) ms:contentKeyID: 48546182 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c138a-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c138a-103"><<<<<<< HEAD</span></span>
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="c138a-104">Propriedade CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="c138a-104">CursorLocation Property (ADO)</span></span>
=======
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="c138a-105">Propriedade CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="c138a-105">CursorLocation property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c138a-106">mestre</span><span class="sxs-lookup"><span data-stu-id="c138a-106">master</span></span>


<span data-ttu-id="c138a-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c138a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c138a-108">Indica o local do serviço de cursor.</span><span class="sxs-lookup"><span data-stu-id="c138a-108">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c138a-109">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c138a-109">Settings And Return Values</span></span>

<span data-ttu-id="c138a-110">Define ou retorna um valor **Long** que pode ser definido como um dos valores [CursorLocationEnum](cursorlocationenum.md).</span><span class="sxs-lookup"><span data-stu-id="c138a-110">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c138a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c138a-111">Remarks</span></span>

<span data-ttu-id="c138a-p101">Essa propriedade permite que você escolha entre diversas bibliotecas de cursores acessíveis ao provedor. Geralmente, é possível escolher entre usar uma biblioteca de cursores do lado do cliente ou uma que esteja localizada no servidor.</span><span class="sxs-lookup"><span data-stu-id="c138a-p101">This property allows you to choose between various cursor libraries accessible to the provider. Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="c138a-p102">A definição dessa propriedade afeta as conexões estabelecidas apenas depois que a propriedade tiver sido configurada. A alteração da propriedade **CursorLocation** não afeta as conexões existentes.</span><span class="sxs-lookup"><span data-stu-id="c138a-p102">This property setting affects connections established only after the property has been set. Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="c138a-p103">Os cursores retornados pelo método [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) herdam essa definição. Os objetos **Recordset** herdarão automaticamente essa definição de suas conexões associadas.</span><span class="sxs-lookup"><span data-stu-id="c138a-p103">Cursors returned by the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method inherit this setting. **Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="c138a-118">Essa propriedade é leitura/gravação em um [Connection](connection-object-ado.md) ou um [Recordset](recordset-object-ado.md) fechado e somente leitura em um **Recordset** aberto.</span><span class="sxs-lookup"><span data-stu-id="c138a-118">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="c138a-119">**Uso de serviço de dados remotos** Quando usado em um cliente **Recordset** ou um objeto de **Conexão** , a propriedade **CursorLocation** só pode ser definida como **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="c138a-119">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

