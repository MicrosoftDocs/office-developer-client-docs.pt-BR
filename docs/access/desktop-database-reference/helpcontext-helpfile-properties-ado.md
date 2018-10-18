---
<span data-ttu-id="f01c7-101"><<<<<<< Título cabeça: HelpContext, HelpFile propriedades (ADO) TOCTitle: HelpContext, HelpFile propriedades (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: ms.date 48546194: 09/18 / 2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="f01c7-101"><<<<<<< HEAD title: HelpContext, HelpFile Properties (ADO) TOCTitle: HelpContext, HelpFile Properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="f01c7-102">Propriedades HelpContext, HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="f01c7-102">HelpContext, HelpFile Properties (ADO)</span></span>

<span data-ttu-id="f01c7-103">=== título: Propriedades HelpContext, HelpFile (ADO) TOCTitle: HelpContext, HelpFile propriedades (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: ms.date 48546194: 10/17/2018 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="f01c7-103">======= title: HelpContext, HelpFile properties (ADO) TOCTitle: HelpContext, HelpFile properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="f01c7-104">Propriedades HelpContext, HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="f01c7-104">HelpContext, HelpFile properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="f01c7-105">mestre</span><span class="sxs-lookup"><span data-stu-id="f01c7-105">master</span></span>

<span data-ttu-id="f01c7-106">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f01c7-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f01c7-107">Indica o arquivo de ajuda e o tópico associado a um objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f01c7-107">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="f01c7-108"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="f01c7-108"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="f01c7-109">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="f01c7-109">Return Values</span></span>

  - <span data-ttu-id="f01c7-110">**HelpContextID**  retorna uma ID de contexto, como um valor **Long**, para um tópico em um arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="f01c7-110">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="f01c7-111">**HelpFile**  retorna um valor **String** que avalia um caminho completamente resolvido para um arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="f01c7-111">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="f01c7-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f01c7-112">Return values</span></span>

- <span data-ttu-id="f01c7-113">**HelpContextID**  retorna uma ID de contexto, como um valor **Long**, para um tópico em um arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="f01c7-113">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="f01c7-114">**HelpFile**  retorna um valor **String** que avalia um caminho completamente resolvido para um arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="f01c7-114">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
>>>>>>> <span data-ttu-id="f01c7-115">mestre</span><span class="sxs-lookup"><span data-stu-id="f01c7-115">master</span></span>

## <a name="remarks"></a><span data-ttu-id="f01c7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f01c7-116">Remarks</span></span>

<span data-ttu-id="f01c7-p101">Se um arquivo de Ajuda for especificado na propriedade **HelpFile**, a propriedade **HelpContext** será usada para exibir automaticamente o tópico de Ajuda que ela identificar. Se não houver um tópico de ajuda relevante disponível, a propriedade **HelpContext** retornará zero e a propriedade **HelpFile** retornará uma sequência de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="f01c7-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

