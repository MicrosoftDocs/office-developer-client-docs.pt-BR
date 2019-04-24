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
description: 'As fórmulas podem conter sequências de caracteres. Para formatar a saída da sequência, como em uma célula de prompt, um valor de item de dados da forma ou um campo de texto, especifique uma figura de formatação. A saída pode ser formatada como um par de unidade numérica, uma sequência de caracteres, uma data ou hora, uma duração ou uma moeda. Por exemplo, o formato picture0 #/10 uuformats o par número da unidade, 10.9 cm As10 9/10 centímetros.'
ms.openlocfilehash: aa95e11db387913edbb40292f7da6a0f4b8a5cf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345063"
---
# <a name="about-strings"></a><span data-ttu-id="331d7-106">Sobre Sequências de Caracteres</span><span class="sxs-lookup"><span data-stu-id="331d7-106">About Strings</span></span>

<span data-ttu-id="331d7-p102">As fórmulas podem conter sequências de caracteres. Para formatar a saída da sequência, como em uma célula de prompt, um valor de item de dados da forma ou um campo de texto, especifique uma figura de formatação. A saída pode ser formatada como um par de unidade numérica, uma sequência de caracteres, uma data ou hora, uma duração ou uma moeda. Por exemplo, a figura de formatação "0 #/10 uu" formata o par de unidade numérica 10,9 cm como "10 9/10 centímetros".</span><span class="sxs-lookup"><span data-stu-id="331d7-p102">Formulas can contain strings. To format string output, such as in a prompt cell, a shape data item value, or a text field, you specify a format picture. Output can be formatted as a number-unit pair, string, date-time, duration, or currency. For example, the format picture "0 #/10 uu" formats the number-unit pair 10.9cm as "10 9/10 centimeters".</span></span>
  
<span data-ttu-id="331d7-111">Você pode usar Format Pictures na célula **Format** da seção Shape data e como um argumento para a função **Format** ou **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="331d7-111">You can use format pictures in the **Format** cell of the Shape Data section and as an argument to the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="331d7-112">Quando você insere um campo de texto, as imagens de formatação são exibidas na lista de formatações da caixa de diálogo **Campo** (guia **Inserir**).</span><span class="sxs-lookup"><span data-stu-id="331d7-112">When you insert a text field, format pictures appear in the list of formats in the **Field** dialog box (**Insert** tab).</span></span> 
  
## <a name="using-functions-to-format-strings"></a><span data-ttu-id="331d7-113">Usando funções para formatar sequências de caracteres</span><span class="sxs-lookup"><span data-stu-id="331d7-113">Using functions to format strings</span></span>

<span data-ttu-id="331d7-114">Em qualquer fórmula que seja resolvida como uma cadeia de caracteres, incluindo fórmulas de campos de texto personalizados, você pode usar a função **Format** ou **FORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="331d7-114">In any formula that resolves to a string, including custom text field formulas, you can use the **FORMAT** or **FORMATEX** function.</span></span> <span data-ttu-id="331d7-115">A função FORMAT retorna uma sequência de caracteres da saída formatada.</span><span class="sxs-lookup"><span data-stu-id="331d7-115">The FORMAT function returns a string of the formatted output.</span></span> <span data-ttu-id="331d7-116">A função **FORMATEX** converte entradas não digitadas nas unidades escolhidas para o resultado formatado.</span><span class="sxs-lookup"><span data-stu-id="331d7-116">The **FORMATEX** function converts untyped input to the units you choose for the formatted result.</span></span> 
  
## <a name="displaying-formatted-shape-data"></a><span data-ttu-id="331d7-117">Exibindo dados de forma formatados</span><span class="sxs-lookup"><span data-stu-id="331d7-117">Displaying formatted shape data</span></span>

<span data-ttu-id="331d7-118">Você pode formatar o valor exibido de um item de dados da forma inserindo uma imagem de formatação na célula Format.</span><span class="sxs-lookup"><span data-stu-id="331d7-118">You can format the displayed value of a shape data item by entering a format picture in the Format cell.</span></span>
  
<span data-ttu-id="331d7-p105">Por exemplo, a forma do cronograma de um projeto pode ter um item de dados da forma para medir o custo de um processo. Como padrão, o valor de um item de dados da forma é uma sequência de caracteres. Para formatar a sequência "1200", você pode inserir "$###,###.00" na célula Format de forma que os usuários possam visualizar uma moeda.</span><span class="sxs-lookup"><span data-stu-id="331d7-p105">For example, a project timeline shape can have a shape data item that measures the cost of a process. By default, a shape data item value is a string. To format the string "1200", you can enter "$###,###.00" in the Format cell so that the user sees a currency.</span></span>
  
<span data-ttu-id="331d7-122">O Microsoft Visio usa as configurações na guia **Moeda** na caixa de diálogo **Personalizar Formato** no item **Região e Idioma** no Painel de Controle para determinar o símbolo da moeda e o separador de milhar a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="331d7-122">Microsoft Visio uses the settings on the **Currency** tab in the **Customize Format** dialog box in the **Region and Language** item in Control Panel to determine the currency symbol and thousands separator to display.</span></span> <span data-ttu-id="331d7-123">No **painel de controle**, clique em **região e idioma**e, em seguida, clique em **configurações adicionais**.</span><span class="sxs-lookup"><span data-stu-id="331d7-123">(In **Control Panel**, click **Region and Language**, and then click **Additional Settings**.)</span></span>
  
<span data-ttu-id="331d7-124">Para converter uma sequência de caracteres no valor de uma moeda, de forma que você possa efetuar cálculos com o valor, use a função CY.</span><span class="sxs-lookup"><span data-stu-id="331d7-124">To convert a string to a currency value so that you can perform calculations with the value, use the CY function.</span></span>
  
## <a name="using-functions-to-manipulate-text-strings"></a><span data-ttu-id="331d7-125">Usando funções para manipular sequências de caracteres de texto</span><span class="sxs-lookup"><span data-stu-id="331d7-125">Using functions to manipulate text strings</span></span>

<span data-ttu-id="331d7-p107">É possível usar funções para manipular sequências de caracteres de texto, por exemplo, para localizar ou substituir determinados caracteres em uma sequência de texto. Além disso, você pode obter informações sobre a posição de um caractere em uma sequência ou identificar os caracteres inicial e final em uma sequência de texto.</span><span class="sxs-lookup"><span data-stu-id="331d7-p107">You can use functions to manipulate text strings, for example, to locate or replace certain characters in a text string. You can also get information about the position of a character in a string, or identify beginning and ending characters in a text string.</span></span> 
  

