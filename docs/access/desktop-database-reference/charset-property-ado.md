---
title: Propriedade Charset (ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca4640940c217fd81cac4ba1d8ffaf769b506fe0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703976"
---
# <a name="charset-property-ado"></a><span data-ttu-id="d321a-102">Propriedade Charset (ADO)</span><span class="sxs-lookup"><span data-stu-id="d321a-102">Charset property (ADO)</span></span>


<span data-ttu-id="d321a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d321a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d321a-104">Indica o conjunto de caracteres no qual o conteúdo de um texto [Stream](stream-object-ado.md) deve ser traduzido para armazenamento no buffer interno dos objetos Stream.</span><span class="sxs-lookup"><span data-stu-id="d321a-104">Indicates the character set into which the contents of a text [Stream](stream-object-ado.md) should be translated for storage in the Stream objects internal buffer.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d321a-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="d321a-105">Settings and return values</span></span>

<span data-ttu-id="d321a-106">Define ou retorna um valor **String** que especifica o conjunto de caracteres no qual o conteúdo do **Stream** será traduzido.</span><span class="sxs-lookup"><span data-stu-id="d321a-106">Sets or returns a **String** value that specifies the character set into which the contents of the **Stream** will be translated.</span></span> <span data-ttu-id="d321a-107">O valor padrão é "Unicode".</span><span class="sxs-lookup"><span data-stu-id="d321a-107">The default value is "Unicode".</span></span> <span data-ttu-id="d321a-108">Os valores permitidos são sequências típicas passadas pela interface como sequências de conjuntos de caracteres para a Internet (por exemplo, "iso-8859-1", "Windows-1252" etc.).</span><span class="sxs-lookup"><span data-stu-id="d321a-108">Allowed values are typical strings passed over the interface as Internet character set strings (for example, "iso-8859-1", "Windows-1252", etc.).</span></span> <span data-ttu-id="d321a-109">Para obter uma lista das sequências de conjunto de caracteres que é conhecida por um sistema, consulte as subchaves da HKEY\_CLASSES\_raiz\\MIME\\banco de dados\\Charset no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="d321a-109">For a list of the character set strings that is known by a system, see the subkeys of HKEY\_CLASSES\_ROOT\\MIME\\Database\\Charset in the Windows Registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="d321a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d321a-110">Remarks</span></span>

<span data-ttu-id="d321a-p102">Em um objeto **Stream** de texto, os dados do texto são armazenados no conjunto de caracteres especificado pela propriedade **Charset**. O padrão é Unicode. A propriedade **Charset** é usada para a conversão de dados que entram no **Stream** ou saem do **Stream**. Por exemplo, se o **Stream** contiver dados ISO-8859-1 e estes forem copiados para um BSTR, o objeto **Stream** converterá os dados em Unicode. O inverso também é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="d321a-p102">In a text **Stream** object, text data is stored in the character set specified by the **Charset** property. The default is Unicode. The **Charset** property is used for converting data going into the **Stream** or coming out of the **Stream**. For example, if the **Stream** contains ISO-8859-1 data and that data is copied to a BSTR, the **Stream** object will convert the data to Unicode. The reverse is also true.</span></span>

<span data-ttu-id="d321a-116">Para um **Stream** aberto, a propriedade [Position](position-property-ado.md) atual deve estar no começo do **Stream** (0) para que seja possível configurar **Charset**.</span><span class="sxs-lookup"><span data-stu-id="d321a-116">For an open **Stream**, the current [Position](position-property-ado.md) must be at the beginning of the **Stream** (0) to be able to set **Charset**.</span></span>

<span data-ttu-id="d321a-p103">**Charset** é usada apenas com objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Essa propriedade será ignorada se **Type** for **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="d321a-p103">**Charset** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

