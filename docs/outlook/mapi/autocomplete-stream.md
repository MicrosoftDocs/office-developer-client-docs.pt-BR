---
title: Fluxo de preenchimento automático
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766223"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="1844a-103">Fluxo de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="1844a-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="1844a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1844a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1844a-105">Além de saber como o Microsoft Outlook interage com o fluxo de preenchimento automático, você deve entender o formato binário do fluxo de AutoCompletar.</span><span class="sxs-lookup"><span data-stu-id="1844a-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="1844a-106">O fluxo de preenchimento automático é um conjunto de linhas de propriedade do destinatário que são salvos como um fluxo binário em conjunto com alguns metadados de escrituração contábil que é usado apenas pelo Microsoft Outlook 2013, o Microsoft Outlook 2010, o Microsoft Office Outlook 2007 e o Microsoft Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="1844a-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="1844a-107">Os metadados são relevantes para interações do Outlook com o fluxo de AutoCompletar para que terceiros deve preservar o que há em cada bloco de metadados quando eles salvam um fluxo de AutoCompletar modificadas.</span><span class="sxs-lookup"><span data-stu-id="1844a-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="1844a-108">Em outras palavras, terceiros deve modificar apenas a parte do conjunto de linhas do formato binário e preservar o que já foi em sobre os blocos de metadados do fluxo de AutoCompletar.</span><span class="sxs-lookup"><span data-stu-id="1844a-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="1844a-109">Visualização de fluxo</span><span class="sxs-lookup"><span data-stu-id="1844a-109">Stream Visualization</span></span>

<span data-ttu-id="1844a-110">O layout de alto nível do fluxo de AutoCompletar é da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1844a-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="1844a-111">Metadados (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="1844a-112">Número da versão principal (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="1844a-113">Número da versão secundária (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="1844a-114">Número de linhas n (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="1844a-115">Número de propriedades p da linha um (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="1844a-116">Marca de propriedade de propriedade do 1 (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="1844a-117">Propriedade 1 reservados da dados (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="1844a-118">União de valor de propriedade do 1 (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="1844a-119">Dados de valor de propriedade do 1 (0 ou variáveis bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="1844a-120">…</span><span class="sxs-lookup"><span data-stu-id="1844a-120"></span></span> <span data-ttu-id="1844a-121">(propriedade 2 por meio da propriedade P-1)</span><span class="sxs-lookup"><span data-stu-id="1844a-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="1844a-122">Marca de propriedade de propriedade do p (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="1844a-123">Propriedade p reservados da dados (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="1844a-124">União de valor de propriedade do p (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="1844a-125">Dados de valor de propriedade do p (0 ou variáveis bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="1844a-126">Número de perguntas de propriedades na linha dois (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="1844a-127">…</span><span class="sxs-lookup"><span data-stu-id="1844a-127"></span></span> <span data-ttu-id="1844a-128">(Propriedades de linha do dois)</span><span class="sxs-lookup"><span data-stu-id="1844a-128">(row two's properties)</span></span>
  
<span data-ttu-id="1844a-129">…</span><span class="sxs-lookup"><span data-stu-id="1844a-129"></span></span> <span data-ttu-id="1844a-130">(linha 3 por meio de linha n-1)</span><span class="sxs-lookup"><span data-stu-id="1844a-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="1844a-131">Número de propriedades r na linha n (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="1844a-132">…</span><span class="sxs-lookup"><span data-stu-id="1844a-132"></span></span> <span data-ttu-id="1844a-133">(linha n's propriedades)</span><span class="sxs-lookup"><span data-stu-id="1844a-133">(row n's properties)</span></span>
  
<span data-ttu-id="1844a-134">Contagem de bytes de informações extras EI (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="1844a-135">Informações extras (bytes EI)</span><span class="sxs-lookup"><span data-stu-id="1844a-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="1844a-136">Metadados (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="1844a-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="1844a-137">Para obter um exemplo de uma estrutura de binário, consulte exemplo binário a [formato de arquivo do Outlook 2003/2007 NK2 e diretrizes de desenvolvedor.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span><span class="sxs-lookup"><span data-stu-id="1844a-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="1844a-138">Layout de alto nível</span><span class="sxs-lookup"><span data-stu-id="1844a-138">High-level Layout</span></span>

<span data-ttu-id="1844a-139">O layout do fluxo de preenchimento automático de modo geral, é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1844a-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="1844a-140">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-140">**Value Data**</span></span>|<span data-ttu-id="1844a-141">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-142">Metadados</span><span class="sxs-lookup"><span data-stu-id="1844a-142">Metadata</span></span>  <br/> |<span data-ttu-id="1844a-143">4</span><span class="sxs-lookup"><span data-stu-id="1844a-143">4</span></span>  <br/> |
|<span data-ttu-id="1844a-144">Número da versão principal</span><span class="sxs-lookup"><span data-stu-id="1844a-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="1844a-145">4</span><span class="sxs-lookup"><span data-stu-id="1844a-145">4</span></span>  <br/> |
|<span data-ttu-id="1844a-146">Número da versão secundária</span><span class="sxs-lookup"><span data-stu-id="1844a-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="1844a-147">4</span><span class="sxs-lookup"><span data-stu-id="1844a-147">4</span></span>  <br/> |
|<span data-ttu-id="1844a-148">Conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="1844a-148">Row-set</span></span>  <br/> |<span data-ttu-id="1844a-149">Variável</span><span class="sxs-lookup"><span data-stu-id="1844a-149">Variable</span></span>  <br/> |
|<span data-ttu-id="1844a-150">Contagem de bytes de informações extras EI</span><span class="sxs-lookup"><span data-stu-id="1844a-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="1844a-151">4</span><span class="sxs-lookup"><span data-stu-id="1844a-151">4</span></span>  <br/> |
|<span data-ttu-id="1844a-152">Informações extras</span><span class="sxs-lookup"><span data-stu-id="1844a-152">Extra information</span></span>  <br/> |<span data-ttu-id="1844a-153">EI</span><span class="sxs-lookup"><span data-stu-id="1844a-153">EI</span></span>  <br/> |
|<span data-ttu-id="1844a-154">Metadados</span><span class="sxs-lookup"><span data-stu-id="1844a-154">Metadata</span></span>  <br/> |<span data-ttu-id="1844a-155">8</span><span class="sxs-lookup"><span data-stu-id="1844a-155">8</span></span>  <br/> |
   
<span data-ttu-id="1844a-156">Ao ler este fluxo, se a versão principal é diferente de 12, então este fluxo deve não leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="1844a-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="1844a-157">A versão secundária atual do stream AutoCompletar é 0, que tem a contagem de bytes de informações extras definida como 0.</span><span class="sxs-lookup"><span data-stu-id="1844a-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="1844a-158">Se a versão secundária é diferente do que 0, então haverá a informação extra que precisa ser lido quando o fluxo de leitura e preservadas durante a criação de fluxo de informações.</span><span class="sxs-lookup"><span data-stu-id="1844a-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="1844a-159">A versão secundária também precisará ser preservada quando o fluxo de gravação.</span><span class="sxs-lookup"><span data-stu-id="1844a-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="1844a-160">Se ambos esses não são preservados, instâncias do Outlook que escreveu a informação extra perderá os dados.</span><span class="sxs-lookup"><span data-stu-id="1844a-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1844a-161">Aplicativos não devem adicionar dados personalizados para o campo de informações extras ou altere a versão secundária encontram essa funcionalidade dar suporte a extensões do Outlook para o formato e extensões de terceiros não arbitrárias.</span><span class="sxs-lookup"><span data-stu-id="1844a-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="1844a-162">Layout do conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="1844a-162">Row-set Layout</span></span>

<span data-ttu-id="1844a-163">O layout do conjunto de linhas é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1844a-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="1844a-164">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-164">**Value Data**</span></span>|<span data-ttu-id="1844a-165">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-166">Número de linhas</span><span class="sxs-lookup"><span data-stu-id="1844a-166">Number of rows</span></span>  <br/> |<span data-ttu-id="1844a-167">4</span><span class="sxs-lookup"><span data-stu-id="1844a-167">4</span></span>  <br/> |
|<span data-ttu-id="1844a-168">Rows</span><span class="sxs-lookup"><span data-stu-id="1844a-168">Rows</span></span>  <br/> |<span data-ttu-id="1844a-169">Variável</span><span class="sxs-lookup"><span data-stu-id="1844a-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="1844a-170">O número de linhas identifica quantas linhas são fornecidos na próxima parte da sequência fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="1844a-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="1844a-171">Layout de linha</span><span class="sxs-lookup"><span data-stu-id="1844a-171">Row Layout</span></span>

<span data-ttu-id="1844a-172">Cada linha está no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="1844a-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="1844a-173">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-173">**Value Data**</span></span>|<span data-ttu-id="1844a-174">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-175">Número de propriedades</span><span class="sxs-lookup"><span data-stu-id="1844a-175">Number of properties</span></span>  <br/> |<span data-ttu-id="1844a-176">4</span><span class="sxs-lookup"><span data-stu-id="1844a-176">4</span></span>  <br/> |
|<span data-ttu-id="1844a-177">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1844a-177">Properties</span></span>  <br/> |<span data-ttu-id="1844a-178">Variável</span><span class="sxs-lookup"><span data-stu-id="1844a-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="1844a-179">O número de propriedades identifica quantos propriedades são fornecidos na próxima parte da sequência fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="1844a-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="1844a-180">Propriedade Layout</span><span class="sxs-lookup"><span data-stu-id="1844a-180">Property Layout</span></span>

<span data-ttu-id="1844a-181">Cada propriedade está no seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="1844a-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="1844a-182">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-182">**Value Data**</span></span>|<span data-ttu-id="1844a-183">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-184">Propriedade Tag</span><span class="sxs-lookup"><span data-stu-id="1844a-184">Property Tag</span></span>  <br/> |<span data-ttu-id="1844a-185">4</span><span class="sxs-lookup"><span data-stu-id="1844a-185">4</span></span>  <br/> |
|<span data-ttu-id="1844a-186">Dados reservado</span><span class="sxs-lookup"><span data-stu-id="1844a-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="1844a-187">4</span><span class="sxs-lookup"><span data-stu-id="1844a-187">4</span></span>  <br/> |
|<span data-ttu-id="1844a-188">União de valor de propriedade</span><span class="sxs-lookup"><span data-stu-id="1844a-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="1844a-189">Dados do valor</span><span class="sxs-lookup"><span data-stu-id="1844a-189">Value Data</span></span>  <br/> |<span data-ttu-id="1844a-190">0 ou variável (dependendo a marca prop)</span><span class="sxs-lookup"><span data-stu-id="1844a-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="1844a-191">Interpretando o valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1844a-191">Interpreting the Property Value</span></span>

<span data-ttu-id="1844a-192">O valor de propriedade Union e os dados de valor são deve ser interpretado com base na marca de propriedade nos primeiros 4 bytes do bloco de propriedade.</span><span class="sxs-lookup"><span data-stu-id="1844a-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="1844a-193">Marca essa propriedade está no mesmo formato apresentado uma marca de propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="1844a-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="1844a-194">Bits 0 a 15 da marca de propriedade são o tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="1844a-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="1844a-195">Bits de 16 a 31 são o identificador da propriedade.</span><span class="sxs-lookup"><span data-stu-id="1844a-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="1844a-196">O tipo de propriedade determina como o restante da propriedade deve ser lido.</span><span class="sxs-lookup"><span data-stu-id="1844a-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="1844a-197">Valor estático</span><span class="sxs-lookup"><span data-stu-id="1844a-197">Static Value</span></span>

<span data-ttu-id="1844a-198">Algumas propriedades não têm nenhum dado de valor e tem somente os dados na União.</span><span class="sxs-lookup"><span data-stu-id="1844a-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="1844a-199">Os seguintes tipos de propriedade (que vêm da marca de propriedade) devem interpretar os dados de propriedade de união de 8 bytes da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1844a-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="1844a-200">**Tipo de prop**</span><span class="sxs-lookup"><span data-stu-id="1844a-200">**Prop Type**</span></span>|<span data-ttu-id="1844a-201">**Interpretação de união de propriedade**</span><span class="sxs-lookup"><span data-stu-id="1844a-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="1844a-202">PT_I2</span></span>  <br/> |<span data-ttu-id="1844a-203">int curto</span><span class="sxs-lookup"><span data-stu-id="1844a-203">short int</span></span>  <br/> |
|<span data-ttu-id="1844a-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1844a-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="1844a-205">Longas</span><span class="sxs-lookup"><span data-stu-id="1844a-205">long</span></span>  <br/> |
|<span data-ttu-id="1844a-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="1844a-206">PT_R4</span></span>  <br/> |<span data-ttu-id="1844a-207">float</span><span class="sxs-lookup"><span data-stu-id="1844a-207">float</span></span>  <br/> |
|<span data-ttu-id="1844a-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="1844a-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="1844a-209">double</span><span class="sxs-lookup"><span data-stu-id="1844a-209">double</span></span>  <br/> |
|<span data-ttu-id="1844a-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1844a-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="1844a-211">int curto</span><span class="sxs-lookup"><span data-stu-id="1844a-211">short int</span></span>  <br/> |
|<span data-ttu-id="1844a-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1844a-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="1844a-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="1844a-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="1844a-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="1844a-214">PT_I8</span></span>  <br/> |<span data-ttu-id="1844a-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="1844a-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="1844a-216">Valores dinâmicos</span><span class="sxs-lookup"><span data-stu-id="1844a-216">Dynamic Values</span></span>

<span data-ttu-id="1844a-217">Outras propriedades têm dados em um bloco de dados do valor após os primeiros 16 bytes que contêm a marca de propriedade, os dados reservados e o valor de propriedade Union.</span><span class="sxs-lookup"><span data-stu-id="1844a-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="1844a-218">Diferentemente dos valores estáticos, os dados armazenados na União 8 bytes valor da propriedade são irrelevantes na leitura.</span><span class="sxs-lookup"><span data-stu-id="1844a-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="1844a-219">Ao escrever, certifique-se de que você preencher essas 8 bytes com algo.</span><span class="sxs-lookup"><span data-stu-id="1844a-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="1844a-220">No entanto, o conteúdo de 8 bytes não é importante.</span><span class="sxs-lookup"><span data-stu-id="1844a-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="1844a-221">Tipo da marca de propriedade dinâmicos valores, determina como interpretar os dados do valor.</span><span class="sxs-lookup"><span data-stu-id="1844a-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="1844a-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="1844a-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="1844a-223">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-223">**Value Data**</span></span>|<span data-ttu-id="1844a-224">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-225">Número de bytes n</span><span class="sxs-lookup"><span data-stu-id="1844a-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1844a-226">4</span><span class="sxs-lookup"><span data-stu-id="1844a-226">4</span></span>  <br/> |
|<span data-ttu-id="1844a-227">Bytes a ser interpretada como uma cadeia de caracteres ANSI (inclui terminador nulo)</span><span class="sxs-lookup"><span data-stu-id="1844a-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="1844a-228">m</span><span class="sxs-lookup"><span data-stu-id="1844a-228">n</span></span>  <br/> |
   
<span data-ttu-id="1844a-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="1844a-229">PT_CLSID</span></span>
  
|<span data-ttu-id="1844a-230">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-230">**Value Data**</span></span>|<span data-ttu-id="1844a-231">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-232">Bytes deve ser interpretado como um GUID</span><span class="sxs-lookup"><span data-stu-id="1844a-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="1844a-233">16</span><span class="sxs-lookup"><span data-stu-id="1844a-233">16</span></span>  <br/> |
|||
   
<span data-ttu-id="1844a-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1844a-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="1844a-235">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-235">**Value Data**</span></span>|<span data-ttu-id="1844a-236">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-237">Número de bytes n</span><span class="sxs-lookup"><span data-stu-id="1844a-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1844a-238">4</span><span class="sxs-lookup"><span data-stu-id="1844a-238">4</span></span>  <br/> |
|<span data-ttu-id="1844a-239">Bytes deve ser interpretado como uma matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="1844a-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="1844a-240">m</span><span class="sxs-lookup"><span data-stu-id="1844a-240">n</span></span>  <br/> |
   
<span data-ttu-id="1844a-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="1844a-241">PT_ERROR</span></span>
  
|<span data-ttu-id="1844a-242">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-242">**Value Data**</span></span>|<span data-ttu-id="1844a-243">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-244">Número de bytes n</span><span class="sxs-lookup"><span data-stu-id="1844a-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1844a-245">4</span><span class="sxs-lookup"><span data-stu-id="1844a-245">4</span></span>  <br/> |
|<span data-ttu-id="1844a-246">Bytes deve ser interpretado como uma matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="1844a-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="1844a-247">m</span><span class="sxs-lookup"><span data-stu-id="1844a-247">n</span></span>  <br/> |
   
<span data-ttu-id="1844a-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="1844a-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="1844a-249">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-249">**Value Data**</span></span>|<span data-ttu-id="1844a-250">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-251">Número de matrizes binários X</span><span class="sxs-lookup"><span data-stu-id="1844a-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="1844a-252">4</span><span class="sxs-lookup"><span data-stu-id="1844a-252">4</span></span>  <br/> |
|<span data-ttu-id="1844a-253">A execução de bytes que contém os X matrizes binários.</span><span class="sxs-lookup"><span data-stu-id="1844a-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="1844a-254">Cada matriz deve ser interpretado exatamente como o byte PT_BINARY executar.</span><span class="sxs-lookup"><span data-stu-id="1844a-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="1844a-255">Variável</span><span class="sxs-lookup"><span data-stu-id="1844a-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="1844a-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010 e Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="1844a-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="1844a-257">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-257">**Value Data**</span></span>|<span data-ttu-id="1844a-258">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-259">Número de sequências de caracteres ANSI X</span><span class="sxs-lookup"><span data-stu-id="1844a-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="1844a-260">4</span><span class="sxs-lookup"><span data-stu-id="1844a-260">4</span></span>  <br/> |
|<span data-ttu-id="1844a-261">Uma sequência de bytes que contém as cadeias de caracteres ANSI X.</span><span class="sxs-lookup"><span data-stu-id="1844a-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="1844a-262">Cada cadeia de caracteres deve ser interpretada exatamente como o byte PT_STRING8 executar.</span><span class="sxs-lookup"><span data-stu-id="1844a-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="1844a-263">Variável</span><span class="sxs-lookup"><span data-stu-id="1844a-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="1844a-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="1844a-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="1844a-265">**Dados do valor**</span><span class="sxs-lookup"><span data-stu-id="1844a-265">**Value Data**</span></span>|<span data-ttu-id="1844a-266">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="1844a-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1844a-267">Número de sequências de caracteres UNICODE X</span><span class="sxs-lookup"><span data-stu-id="1844a-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="1844a-268">4</span><span class="sxs-lookup"><span data-stu-id="1844a-268">4</span></span>  <br/> |
|<span data-ttu-id="1844a-269">Uma sequência de bytes que contém X UNICODE cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1844a-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="1844a-270">Cada cadeia de caracteres deve ser interpretada exatamente como o byte PT_UNICODE executar.</span><span class="sxs-lookup"><span data-stu-id="1844a-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="1844a-271">Variável</span><span class="sxs-lookup"><span data-stu-id="1844a-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="1844a-272">Propriedades significativas</span><span class="sxs-lookup"><span data-stu-id="1844a-272">Significant properties</span></span>

<span data-ttu-id="1844a-273">Conforme mencionado anteriormente neste tópico, os blocos de binários que representam propriedades têm marcas de propriedade que correspondem às propriedades nos destinatários de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="1844a-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="1844a-274">Para propriedades que não estão listadas aqui, você pode consultar a descrição da propriedade em http://msdn.microsoft.com/pt-br/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="1844a-274">For properties that are not listed here, you can look up the property description at http://msdn.microsoft.com/pt-br/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="1844a-275">**Nome da propriedade**</span><span class="sxs-lookup"><span data-stu-id="1844a-275">**Property Name**</span></span>|<span data-ttu-id="1844a-276">**Propriedade Tag**</span><span class="sxs-lookup"><span data-stu-id="1844a-276">**Property Tag**</span></span>|<span data-ttu-id="1844a-277">**Descrição (consulte o MSDN para obter mais informações)**</span><span class="sxs-lookup"><span data-stu-id="1844a-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1844a-278">PR_NICK_NAME_W (não transmitidas nos destinatários, específicos de fluxo de AutoCompletar apenas)</span><span class="sxs-lookup"><span data-stu-id="1844a-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1844a-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="1844a-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="1844a-280">Esta propriedade deve ser o primeira em cada linha de destinatário.</span><span class="sxs-lookup"><span data-stu-id="1844a-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="1844a-281">Funcionalmente, ela serve como um identificador de chave para a linha de destinatário.</span><span class="sxs-lookup"><span data-stu-id="1844a-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="1844a-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1844a-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="1844a-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="1844a-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="1844a-284">O identificador de entrada de catálogo de endereços para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="1844a-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="1844a-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1844a-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="1844a-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="1844a-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="1844a-287">Nome para exibição do destinatário.</span><span class="sxs-lookup"><span data-stu-id="1844a-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="1844a-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="1844a-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="1844a-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="1844a-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="1844a-290">Endereço de email do destinatário (por exemplo, johndoe@contoso.com ou /o = Contoso/OU = Foo/cn = Recipients/cn = johndoe)</span><span class="sxs-lookup"><span data-stu-id="1844a-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="1844a-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="1844a-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="1844a-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="1844a-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="1844a-293">Tipo de endereço do destinatário (por exemplo, SMTP ou EX).</span><span class="sxs-lookup"><span data-stu-id="1844a-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="1844a-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="1844a-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="1844a-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="1844a-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="1844a-296">Chave de pesquisa MAPI do destinatário.</span><span class="sxs-lookup"><span data-stu-id="1844a-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="1844a-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="1844a-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="1844a-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="1844a-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="1844a-299">Endereço de SMTP do destinatário.</span><span class="sxs-lookup"><span data-stu-id="1844a-299">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="1844a-300">PR_DROPDOWN_DISPLAY_NAME_W (não transmitidas nos destinatários, específicos de fluxo de AutoCompletar apenas)</span><span class="sxs-lookup"><span data-stu-id="1844a-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1844a-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="1844a-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="1844a-302">A cadeia de caracteres de exibição que aparece na lista AutoCompletar.</span><span class="sxs-lookup"><span data-stu-id="1844a-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="1844a-303">PR_NICK_NAME_WEIGHT (não transmitidas nos destinatários, específicos de fluxo de AutoCompletar apenas)</span><span class="sxs-lookup"><span data-stu-id="1844a-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1844a-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="1844a-304">0x60040003</span></span>  <br/> |<span data-ttu-id="1844a-305">A espessura dessa entrada de AutoCompletar.</span><span class="sxs-lookup"><span data-stu-id="1844a-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="1844a-306">O peso é usado para determinar em qual ordem de AutoCompletar ocorrer entradas na lista AutoCompletar de correspondência.</span><span class="sxs-lookup"><span data-stu-id="1844a-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="1844a-307">Entradas com peso maior mostrará antes de entradas com peso mais baixo.</span><span class="sxs-lookup"><span data-stu-id="1844a-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="1844a-308">A lista completa de AutoCompletar é classificada por esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="1844a-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="1844a-309">O peso periodicamente diminui ao longo do tempo e aumenta quando o usuário envia um email para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="1844a-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="1844a-310">Consulte a descrição neste tópico para obter mais informações sobre essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1844a-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="1844a-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="1844a-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="1844a-312">O conjunto de linhas no stream AutoCompletar é classificado em ordem decrescente pela propriedade PR_NICK_NAME_WEIGHT e o fluxo de AutoCompletar sempre deve preservar essa característica classificada.</span><span class="sxs-lookup"><span data-stu-id="1844a-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="1844a-313">Portanto, quaisquer alterações para espessura da linha um também devem assegurar que a posição da linha mantém a ordem de classificação do conjunto completo de linhas.</span><span class="sxs-lookup"><span data-stu-id="1844a-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="1844a-314">Quaisquer adições para o conjunto de linhas devem ser inseridas na posição correta para manter a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="1844a-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="1844a-315">O valor mínimo desse peso é 0x1 e o valor máximo é LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="1844a-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="1844a-316">Todos os outros valores para o peso são considerados inválidos.</span><span class="sxs-lookup"><span data-stu-id="1844a-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="1844a-317">Quando o Outlook 2007 envia um email para ou resolve um destinatário, ele será aumentado peso do destinatário que em 0x2000.</span><span class="sxs-lookup"><span data-stu-id="1844a-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

