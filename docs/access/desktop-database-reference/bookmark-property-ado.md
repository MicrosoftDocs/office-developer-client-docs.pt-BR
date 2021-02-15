---
title: Propriedade Bookmark (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 17818fe2b4f826cbcfbbb3955817c2b5d99ab6a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296791"
---
# <a name="bookmark-property-ado"></a><span data-ttu-id="b38ed-102">Propriedade Bookmark (ADO)</span><span class="sxs-lookup"><span data-stu-id="b38ed-102">Bookmark property (ADO)</span></span>


<span data-ttu-id="b38ed-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b38ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b38ed-104">Aponta um indicador que identifica com exclusividade o registro atual em um objeto [Recordset](recordset-object-ado.md) ou define o registro atual em um objeto **Recordset** para o registro identificado por um indicador válido.</span><span class="sxs-lookup"><span data-stu-id="b38ed-104">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b38ed-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b38ed-105">Settings and return values</span></span>

<span data-ttu-id="b38ed-106">Configura ou retorna uma expressão **Variant** que avalia um indicador válido.</span><span class="sxs-lookup"><span data-stu-id="b38ed-106">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="b38ed-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b38ed-107">Remarks</span></span>

<span data-ttu-id="b38ed-p101">Use a propriedade **Bookmark** para salvar a posição do registro atual e retornar para esse registro a qualquer momento. Bookmarks estão disponíveis apenas em objetos **Recordset** que ofereçam suporte à funcionalidade de indicadores.</span><span class="sxs-lookup"><span data-stu-id="b38ed-p101">Use the **Bookmark** property to save the position of the current record and return to that record at any time. Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="b38ed-p102">Quando um objeto **Recordset** é aberto, cada um dos registros tem um indicador exclusivo. Para salvar o indicador do registro atual, atribua o valor da propriedade **Bookmark** a uma variável. Para retornar rapidamente àquele registro depois de se mover para um registro diferente, defina a propriedade **Bookmark** do objeto **Recordset** com o valor daquela variável.</span><span class="sxs-lookup"><span data-stu-id="b38ed-p102">When you open a **Recordset** object, each of its records has a unique bookmark. To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="b38ed-p103">Talvez o usuário não seja capaz de exibir o valor do indicador. Além disso, os usuários não devem esperar que os indicadores sejam comparados diretamente  dois indicadores referentes ao mesmo registro podem ter valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="b38ed-p103">The user may not be able to view the value of the bookmark. Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="b38ed-p104">Se você usar o método [Clone](clone-method-ado.md) para criar uma cópia de um objeto **Recordset**, as definições da propriedade **Bookmark** para os objetos **Recordset** original e duplicado serão idênticas e você poderá usá-las alternadamente. Contudo, não é possível usar indicadores de objetos **Recordset** diferentes alternadamente, mesmo que eles tenham sido criados a partir da mesma fonte ou comando.</span><span class="sxs-lookup"><span data-stu-id="b38ed-p104">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably. However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="b38ed-117">**Uso do Remote Data Service** Quando usada em um objeto **Recordset** do lado do cliente, a propriedade **Bookmark** está sempre disponível.</span><span class="sxs-lookup"><span data-stu-id="b38ed-117">**Remote Data Service Usage** When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

