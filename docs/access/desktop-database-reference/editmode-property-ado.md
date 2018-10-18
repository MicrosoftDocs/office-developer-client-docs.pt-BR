---
<span data-ttu-id="ca725-101"><<<<<<< Título cabeça: propriedade EditMode (ADO) TOCTitle: propriedade EditMode (ADO) === título: propriedade EditMode (ADO) TOCTitle: propriedade EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ca725-101"><<<<<<< HEAD title: EditMode Property (ADO) TOCTitle: EditMode Property (ADO) ======= title: EditMode property (ADO) TOCTitle: EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ca725-102">ms:assetid de mestre: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: ms.date 48543867: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ca725-102">master ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: 48543867 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ca725-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ca725-103"><<<<<<< HEAD</span></span>
# <a name="editmode-property-ado"></a><span data-ttu-id="ca725-104">Propriedade EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ca725-104">EditMode Property (ADO)</span></span>
=======
# <a name="editmode-property-ado"></a><span data-ttu-id="ca725-105">Propriedade EditMode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ca725-105">EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ca725-106">mestre</span><span class="sxs-lookup"><span data-stu-id="ca725-106">master</span></span>


<span data-ttu-id="ca725-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca725-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ca725-108">Indica o status de edição do registro atual.</span><span class="sxs-lookup"><span data-stu-id="ca725-108">Indicates the editing status of the current record.</span></span>

<span data-ttu-id="ca725-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ca725-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="ca725-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ca725-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="ca725-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ca725-111">Return value</span></span>
>>>>>>> <span data-ttu-id="ca725-112">mestre</span><span class="sxs-lookup"><span data-stu-id="ca725-112">master</span></span>

<span data-ttu-id="ca725-113">Retorna um valor [EditModeEnum](editmodeenum.md).</span><span class="sxs-lookup"><span data-stu-id="ca725-113">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca725-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca725-114">Remarks</span></span>

<span data-ttu-id="ca725-p101">O ADO mantém um buffer de edição associado ao registro atual. Essa propriedade indica se as alterações foram feitas nesse buffer ou se um novo registro foi criado. Use a propriedade **EditMode** para determinar o status de edição do registro atual. É possível procurar alterações pendentes se um processo de edição tiver sido interrompido e determinar se você precisa usar o método [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ca725-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="ca725-119">Consulte o método [AddNew](addnew-method-ado.md) para obter uma descrição mais detalhada da propriedade **EditMode** em diferentes condições de edição.</span><span class="sxs-lookup"><span data-stu-id="ca725-119">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="ca725-120">Quando uma chamada para [Excluir](delete-method-ado-recordset.md) não exclui o registro com êxito ou registros nos dados de origem (devido a violações de integridade referencial, por exemplo), o [Recordset](recordset-object-ado.md) permanecerá no modo de edição (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="ca725-120">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="ca725-121">Isso significa que **CancelUpdate** deve ser chamado antes de sair do registro atual (com [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md), por exemplo).</span><span class="sxs-lookup"><span data-stu-id="ca725-121">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <P><span data-ttu-id="ca725-p103">[!OBSERVAçãO] <STRONG>EditMode</STRONG> pode retornar um valor válido apenas se existir um registro atual. O <STRONG>EditMode</STRONG> retornará um erro se <A href="bof-eof-properties-ado.md">BOF ou EOF</A> for verdadeiro ou se o registro atual tiver sido excluído.</span><span class="sxs-lookup"><span data-stu-id="ca725-p103"><STRONG>EditMode</STRONG> can return a valid value only if there is a current record. <STRONG>EditMode</STRONG> will return an error if <A href="bof-eof-properties-ado.md">BOF or EOF</A> is true, or if the current record has been deleted.</span></span></P>


