---
title: Sobre Sequências de Caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251826
localization_priority: Normal
ms.assetid: e1174d8f-70cb-4595-7906-889da15367db
description: 'Fórmulas que podem conter cadeias de caracteres. Para formatar a saída de cadeia de caracteres, como em uma célula prompt, um valor de item de dados da forma ou um campo de texto, você deve especificar uma figura de formatação. Saída pode ser formatada como um par de unidade numérica, cadeia de caracteres, data / hora, duração ou uma moeda. Por exemplo, os uuformats de #/ 10 formato picture0 a unidade de número emparelhar 10,9 cm as10 9/10 centímetros.'
ms.openlocfilehash: 1fd003ecd5c824042e97a40fa8374aeead254ddc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771227"
---
# <a name="about-strings"></a><span data-ttu-id="65e23-106">Sobre cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="65e23-106">About Strings</span></span>

<span data-ttu-id="65e23-p102">As fórmulas podem conter sequências de caracteres. Para formatar a saída da sequência, como em uma célula de prompt, um valor de item de dados da forma ou um campo de texto, especifique uma figura de formatação. A saída pode ser formatada como um par de unidade numérica, uma sequência de caracteres, uma data ou hora, uma duração ou uma moeda. Por exemplo, a figura de formatação "0 #/10 uu" formata o par de unidade numérica 10,9 cm como "10 9/10 centímetros".</span><span class="sxs-lookup"><span data-stu-id="65e23-p102">Formulas can contain strings. To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture. Output can be formatted as a number-unit pair, string, date-time, duration, or currency. For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="65e23-111">Você pode usar figuras de formatação na célula **Format** da seção dados da forma e como um argumento para a função **FORMAT** ou **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="65e23-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="65e23-112">Quando você insere um campo de texto, figuras de formatação aparecem na lista de formatos na caixa de diálogo **campo** (guia**Inserir** ).</span><span class="sxs-lookup"><span data-stu-id="65e23-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="65e23-113">Usando funções para formatar sequências de caracteres</span><span class="sxs-lookup"><span data-stu-id="65e23-113">Using functions to format strings</span></span>

<span data-ttu-id="65e23-114">Em qualquer fórmula que resulta em uma cadeia de caracteres, incluindo fórmulas de campo de texto personalizado, você pode usar a função **FORMAT** ou **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="65e23-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="65e23-115">A função FORMAT retorna uma cadeia de caracteres da saída formatada.</span><span class="sxs-lookup"><span data-stu-id="65e23-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="65e23-116">A função **FORMATEX** converte a entrada não digitada para as unidades que você escolher para o resultado formatado.</span><span class="sxs-lookup"><span data-stu-id="65e23-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="65e23-117">Exibindo dados de forma formatados</span><span class="sxs-lookup"><span data-stu-id="65e23-117">Displaying formatted shape data</span></span>

<span data-ttu-id="65e23-118">Você pode formatar o valor exibido de um item de dados da forma inserindo uma imagem de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="65e23-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="65e23-p105">Por exemplo, a forma do cronograma de um projeto pode ter um item de dados da forma para medir o custo de um processo. Como padrão, o valor de um item de dados da forma é uma sequência de caracteres. Para formatar a sequência "1200", você pode inserir "$###,###.00" na célula Format de forma que os usuários possam visualizar uma moeda.</span><span class="sxs-lookup"><span data-stu-id="65e23-p105">For example, a project timeline shape can have a shape data item that measures the cost of a process. By default, a shape data item value is a string. To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="65e23-122">Microsoft Visio utiliza as configurações na guia **moeda** , na caixa de diálogo **Personalizar formato** no item de **região e idioma** no painel de controle para determinar o símbolo de moeda e de milhar separador para exibir.</span><span class="sxs-lookup"><span data-stu-id="65e23-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="65e23-123">(No **Painel de controle**, clique em **região e idioma**e, em seguida, clique em **Configurações adicionais**).</span><span class="sxs-lookup"><span data-stu-id="65e23-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="65e23-124">Para converter uma sequência de caracteres no valor de uma moeda, de forma que você possa efetuar cálculos com o valor, use a função CY.</span><span class="sxs-lookup"><span data-stu-id="65e23-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="65e23-125">Usando funções para manipular sequências de caracteres de texto</span><span class="sxs-lookup"><span data-stu-id="65e23-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="65e23-p107">É possível usar funções para manipular sequências de caracteres de texto, por exemplo, para localizar ou substituir determinados caracteres em uma sequência de texto. Além disso, você pode obter informações sobre a posição de um caractere em uma sequência ou identificar os caracteres inicial e final em uma sequência de texto.</span><span class="sxs-lookup"><span data-stu-id="65e23-p107">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string. You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

