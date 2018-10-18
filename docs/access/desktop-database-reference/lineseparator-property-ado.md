---
<span data-ttu-id="a2910-101"><<<<<<< Título cabeça: propriedade LineSeparator (ADO) TOCTitle: propriedade LineSeparator (ADO) === título: propriedade LineSeparator (ADO) TOCTitle: propriedade LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2910-101"><<<<<<< HEAD title: LineSeparator Property (ADO) TOCTitle: LineSeparator Property (ADO) ======= title: LineSeparator property (ADO) TOCTitle: LineSeparator property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a2910-102">ms:assetid de mestre: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: ms.date 48546676: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a2910-102">master ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) ms:contentKeyID: 48546676 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a2910-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="a2910-103"><<<<<<< HEAD</span></span>
# <a name="lineseparator-property-ado"></a><span data-ttu-id="a2910-104">Propriedade LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2910-104">LineSeparator Property (ADO)</span></span>
=======
# <a name="lineseparator-property-ado"></a><span data-ttu-id="a2910-105">Propriedade LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="a2910-105">LineSeparator property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a2910-106">mestre</span><span class="sxs-lookup"><span data-stu-id="a2910-106">master</span></span>


<span data-ttu-id="a2910-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2910-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a2910-108">Indica o caractere binário a ser usado como o separador de linha nos objetos [Stream](stream-object-ado.md) de texto.</span><span class="sxs-lookup"><span data-stu-id="a2910-108">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

<span data-ttu-id="a2910-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="a2910-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="a2910-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a2910-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="a2910-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a2910-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="a2910-112">mestre</span><span class="sxs-lookup"><span data-stu-id="a2910-112">master</span></span>

<span data-ttu-id="a2910-p101">Define ou retorna um valor [LineSeparatorsEnum](lineseparatorsenum.md) que indica o caractere do separador de linha usado no **Stream**. O valor padrão é **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="a2910-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2910-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2910-115">Remarks</span></span>

<span data-ttu-id="a2910-p102">**LineSeparator** é usada para interpretar as linhas ao ler o conteúdo de um **Stream** de texto. As linhas podem ser ignoradas com o método [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a2910-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="a2910-p103">**LineSeparator** é usada apenas com objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Esta propriedade será ignorada se **Type** for **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="a2910-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

