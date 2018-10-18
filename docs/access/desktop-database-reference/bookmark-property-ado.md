---
<span data-ttu-id="ffdbf-101"><<<<<<< Título cabeça: propriedade Bookmark (ADO) TOCTitle: propriedade Bookmark (ADO) === título: propriedade Bookmark (ADO) TOCTitle: propriedade Bookmark (ADO)</span><span class="sxs-lookup"><span data-stu-id="ffdbf-101"><<<<<<< HEAD title: Bookmark Property (ADO) TOCTitle: Bookmark Property (ADO) ======= title: Bookmark property (ADO) TOCTitle: Bookmark property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ffdbf-102">ms:assetid de mestre: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15) ms:contentKeyID: ms.date 48543287: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ffdbf-102">master ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15) ms:contentKeyID: 48543287 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ffdbf-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ffdbf-103"><<<<<<< HEAD</span></span>
# <a name="bookmark-property-ado"></a><span data-ttu-id="ffdbf-104">Propriedade Bookmark (ADO)</span><span class="sxs-lookup"><span data-stu-id="ffdbf-104">Bookmark Property (ADO)</span></span>
=======
# <a name="bookmark-property-ado"></a><span data-ttu-id="ffdbf-105">Propriedade Bookmark (ADO)</span><span class="sxs-lookup"><span data-stu-id="ffdbf-105">Bookmark property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ffdbf-106">mestre</span><span class="sxs-lookup"><span data-stu-id="ffdbf-106">master</span></span>


<span data-ttu-id="ffdbf-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffdbf-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ffdbf-108">Aponta um indicador que identifica com exclusividade o registro atual em um objeto [Recordset](recordset-object-ado.md) ou define o registro atual em um objeto **Recordset** para o registro identificado por um indicador válido.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-108">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

<span data-ttu-id="ffdbf-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ffdbf-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="ffdbf-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ffdbf-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="ffdbf-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ffdbf-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="ffdbf-112">mestre</span><span class="sxs-lookup"><span data-stu-id="ffdbf-112">master</span></span>

<span data-ttu-id="ffdbf-113">Configura ou retorna uma expressão **Variant** que avalia um indicador válido.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-113">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffdbf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffdbf-114">Remarks</span></span>

<span data-ttu-id="ffdbf-p101">Use a propriedade **Bookmark** para salvar a posição do registro atual e retornar para esse registro a qualquer momento. Bookmarks estão disponíveis apenas em objetos **Recordset** que ofereçam suporte à funcionalidade de indicadores.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-p101">Use the **Bookmark** property to save the position of the current record and return to that record at any time. Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="ffdbf-p102">Quando um objeto **Recordset** é aberto, cada um dos registros tem um indicador exclusivo. Para salvar o indicador do registro atual, atribua o valor da propriedade **Bookmark** a uma variável. Para retornar rapidamente àquele registro depois de se mover para um registro diferente, defina a propriedade **Bookmark** do objeto **Recordset** com o valor daquela variável.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-p102">When you open a **Recordset** object, each of its records has a unique bookmark. To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="ffdbf-p103">Talvez o usuário não seja capaz de exibir o valor do indicador. Além disso, os usuários não devem esperar que os indicadores sejam comparados diretamente  dois indicadores referentes ao mesmo registro podem ter valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-p103">The user may not be able to view the value of the bookmark. Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="ffdbf-p104">Se você usar o método [Clone](clone-method-ado.md) para criar uma cópia de um objeto **Recordset**, as definições da propriedade **Bookmark** para os objetos **Recordset** original e duplicado serão idênticas e você poderá usá-las alternadamente. Contudo, não é possível usar indicadores de objetos **Recordset** diferentes alternadamente, mesmo que eles tenham sido criados a partir da mesma fonte ou comando.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-p104">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably. However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="ffdbf-124">**Uso de serviço de dados remotos** Quando usado em um objeto **Recordset** do lado do cliente, a propriedade **Bookmark** está sempre disponível.</span><span class="sxs-lookup"><span data-stu-id="ffdbf-124">**Remote Data Service Usage**When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

