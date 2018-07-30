---
title: Fluxo de preenchimento automático
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766223"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="53873-103">Fluxo de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="53873-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="53873-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53873-104">**Applies to:** Outlook \*</span></span> 
  
<span data-ttu-id="53873-105">Além de saber como o Microsoft Outlook interage com o fluxo de preenchimento automático, você também deve entender formato binário dele.</span><span class="sxs-lookup"><span data-stu-id="53873-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="53873-106">O fluxo de preenchimento automático é um conjunto de linhas de propriedade de destinatário salvo como um fluxo de binário com alguns metadados contábeis usados apenas pelo Microsoft Outlook 2013, o Microsoft Outlook 2010, o Microsoft Office Outlook 2007 e o Microsoft Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="53873-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="53873-107">Os metadados são relevantes para as interações do Outlook com o fluxo de preenchimento automático, assim terceiros devem manter o que está em cada bloco de metadados quando salvam um fluxo de preenchimento automático modificado.</span><span class="sxs-lookup"><span data-stu-id="53873-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="53873-108">Em outras palavras, terceiros devem modificar apenas a parte do conjunto de linhas do formato binário e preservar o que já estava nos blocos de metadados do fluxo de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="53873-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="53873-109">Visualização de Fluxo</span><span class="sxs-lookup"><span data-stu-id="53873-109">Stream Visualization</span></span>

<span data-ttu-id="53873-110">O layout de alto nível do fluxo de preenchimento automático é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="53873-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="53873-111">Metadados (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="53873-112">Número da Versão Principal (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="53873-113">Número da Versão Secundária (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="53873-114">Número de linhas n (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="53873-115">Número de propriedades p na linha um (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="53873-116">Marca da propriedade 1 (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="53873-117">Dados reservados da propriedade 1 (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="53873-118">União de valor da propriedade 1 (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="53873-119">Dados de valor da propriedade 1 (0 byte ou bytes variáveis)</span><span class="sxs-lookup"><span data-stu-id="53873-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="53873-120">…</span><span class="sxs-lookup"><span data-stu-id="53873-120"></span></span> <span data-ttu-id="53873-121">(da propriedade 2 à propriedade P-1)</span><span class="sxs-lookup"><span data-stu-id="53873-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="53873-122">Marca da propriedade p (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="53873-123">Dados reservados da propriedade p (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="53873-124">União de valor da propriedade p (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="53873-125">Dados de valor da propriedade p (0 byte ou bytes variáveis)</span><span class="sxs-lookup"><span data-stu-id="53873-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="53873-126">Número de propriedades q na linha dois (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="53873-127">…</span><span class="sxs-lookup"><span data-stu-id="53873-127"></span></span> <span data-ttu-id="53873-128">(propriedades da linha dois)</span><span class="sxs-lookup"><span data-stu-id="53873-128">(row two's properties)</span></span>
  
<span data-ttu-id="53873-129">…</span><span class="sxs-lookup"><span data-stu-id="53873-129"></span></span> <span data-ttu-id="53873-130">(da linha 3 à linha n-1)</span><span class="sxs-lookup"><span data-stu-id="53873-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="53873-131">Número de propriedades r na linha n (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="53873-132">…</span><span class="sxs-lookup"><span data-stu-id="53873-132"></span></span> <span data-ttu-id="53873-133">(propriedades da linha n)</span><span class="sxs-lookup"><span data-stu-id="53873-133">(row n's properties)</span></span>
  
<span data-ttu-id="53873-134">EI de contagem de bytes de informações extras (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="53873-135">Informações extras (bytes EI)</span><span class="sxs-lookup"><span data-stu-id="53873-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="53873-136">Metadados (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="53873-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="53873-137">Para ver um exemplo de estrutura binária, confira o Exemplo Binário nas [Diretrizes para Desenvolvedor e Formato de Arquivo do Outlook 2003/2007 NK2.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span><span class="sxs-lookup"><span data-stu-id="53873-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="53873-138">Layout de Alto Nível</span><span class="sxs-lookup"><span data-stu-id="53873-138">High-level Layout</span></span>

<span data-ttu-id="53873-139">Em geral, o layout do fluxo de preenchimento automático é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="53873-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="53873-140">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-140">**Value Data**</span></span>|<span data-ttu-id="53873-141">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-142">Metadados</span><span class="sxs-lookup"><span data-stu-id="53873-142">metadata</span></span>  <br/> |<span data-ttu-id="53873-143">4</span><span class="sxs-lookup"><span data-stu-id="53873-143">-4</span></span>  <br/> |
|<span data-ttu-id="53873-144">Número da Versão Principal</span><span class="sxs-lookup"><span data-stu-id="53873-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="53873-145">4</span><span class="sxs-lookup"><span data-stu-id="53873-145">-4</span></span>  <br/> |
|<span data-ttu-id="53873-146">Número da Versão Secundária</span><span class="sxs-lookup"><span data-stu-id="53873-146">Minor version number</span></span>  <br/> |<span data-ttu-id="53873-147">4</span><span class="sxs-lookup"><span data-stu-id="53873-147">-4</span></span>  <br/> |
|<span data-ttu-id="53873-148">Conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="53873-148">Rowset.</span></span>  <br/> |<span data-ttu-id="53873-149">Variável</span><span class="sxs-lookup"><span data-stu-id="53873-149">Variable</span></span>  <br/> |
|<span data-ttu-id="53873-150">EI de contagem de bytes de informações extras</span><span class="sxs-lookup"><span data-stu-id="53873-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="53873-151">4</span><span class="sxs-lookup"><span data-stu-id="53873-151">-4</span></span>  <br/> |
|<span data-ttu-id="53873-152">Informações extras</span><span class="sxs-lookup"><span data-stu-id="53873-152">Extra information</span></span>  <br/> |<span data-ttu-id="53873-153">EI</span><span class="sxs-lookup"><span data-stu-id="53873-153">EI</span></span>  <br/> |
|<span data-ttu-id="53873-154">Metadados</span><span class="sxs-lookup"><span data-stu-id="53873-154">metadata</span></span>  <br/> |<span data-ttu-id="53873-155">8</span><span class="sxs-lookup"><span data-stu-id="53873-155">-8</span></span>  <br/> |
   
<span data-ttu-id="53873-156">Ao ler este fluxo, se a versão principal for diferente da 12, então ele não deverá ser lido nem gravado.</span><span class="sxs-lookup"><span data-stu-id="53873-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="53873-157">A versão secundária atual do fluxo de preenchimento automático é 0, que tem a contagem de Bytes de Informações Extras definida como 0.</span><span class="sxs-lookup"><span data-stu-id="53873-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="53873-158">Se a versão secundária for diferente de 0, então as informações extras apresentarão informações que precisam ser lidas na leitura do fluxo e preservadas na gravação do fluxo.</span><span class="sxs-lookup"><span data-stu-id="53873-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="53873-159">A versão secundária também deverá ser preservada ao gravar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="53873-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="53873-160">Se ambas não forem preservadas, as instâncias do Outlook que gravarem informações extras perderão os dados.</span><span class="sxs-lookup"><span data-stu-id="53873-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="53873-161">Aplicativos não devem adicionar dados personalizados ao campo Informações Extras nem alterar a versão secundária, já que esta funcionalidade existe para dar suporte ao formato de extensões do Outlook e a extensões não arbitrárias de terceiros.</span><span class="sxs-lookup"><span data-stu-id="53873-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="53873-162">Layout de conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="53873-162">Row-set Layout</span></span>

<span data-ttu-id="53873-163">O layout do conjunto de linhas é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="53873-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="53873-164">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-164">**Value Data**</span></span>|<span data-ttu-id="53873-165">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-166">Número de linhas</span><span class="sxs-lookup"><span data-stu-id="53873-166">Number of rows</span></span>  <br/> |<span data-ttu-id="53873-167">4</span><span class="sxs-lookup"><span data-stu-id="53873-167">-4</span></span>  <br/> |
|<span data-ttu-id="53873-168">Linhas</span><span class="sxs-lookup"><span data-stu-id="53873-168">Rows</span></span>  <br/> |<span data-ttu-id="53873-169">Variável</span><span class="sxs-lookup"><span data-stu-id="53873-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="53873-170">O número de linhas identifica quantas linhas existem na próxima parte da sequência de fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="53873-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="53873-171">Layout de Linha</span><span class="sxs-lookup"><span data-stu-id="53873-171">Row Layout</span></span>

<span data-ttu-id="53873-172">Cada linha tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="53873-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="53873-173">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-173">**Value Data**</span></span>|<span data-ttu-id="53873-174">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-175">Número de Propriedades</span><span class="sxs-lookup"><span data-stu-id="53873-175">Number of properties</span></span>  <br/> |<span data-ttu-id="53873-176">4</span><span class="sxs-lookup"><span data-stu-id="53873-176">-4</span></span>  <br/> |
|<span data-ttu-id="53873-177">Propriedades</span><span class="sxs-lookup"><span data-stu-id="53873-177">Properties</span></span>  <br/> |<span data-ttu-id="53873-178">Variável</span><span class="sxs-lookup"><span data-stu-id="53873-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="53873-179">O número de propriedades identifica quantas propriedades existem na próxima parte da sequência de fluxo binário.</span><span class="sxs-lookup"><span data-stu-id="53873-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="53873-180">Layout de Propriedade</span><span class="sxs-lookup"><span data-stu-id="53873-180">Layout Property</span></span>

<span data-ttu-id="53873-181">Cada propriedade tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="53873-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="53873-182">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-182">**Value Data**</span></span>|<span data-ttu-id="53873-183">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-184">Marca de Propriedade</span><span class="sxs-lookup"><span data-stu-id="53873-184">Tag Property</span></span>  <br/> |<span data-ttu-id="53873-185">4</span><span class="sxs-lookup"><span data-stu-id="53873-185">-4</span></span>  <br/> |
|<span data-ttu-id="53873-186">Dados Reservados</span><span class="sxs-lookup"><span data-stu-id="53873-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="53873-187">4</span><span class="sxs-lookup"><span data-stu-id="53873-187">-4</span></span>  <br/> |
|<span data-ttu-id="53873-188">União do Valor da Propriedade</span><span class="sxs-lookup"><span data-stu-id="53873-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="53873-189">Dados do Valor</span><span class="sxs-lookup"><span data-stu-id="53873-189">Value Data</span></span>  <br/> |<span data-ttu-id="53873-190">0 ou variável (dependendo da marca propr)</span><span class="sxs-lookup"><span data-stu-id="53873-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="53873-191">Interpretar o Valor da Propriedade</span><span class="sxs-lookup"><span data-stu-id="53873-191">Interpreting the Property Value</span></span>

<span data-ttu-id="53873-192">A União do Valor da Propriedade e os Dados de Valor são interpretados com base na marca de propriedade dos primeiros 4 bytes do bloco de propriedade.</span><span class="sxs-lookup"><span data-stu-id="53873-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="53873-193">Essa marca de propriedade está no mesmo formato de uma marca de propriedade MAPI.</span><span class="sxs-lookup"><span data-stu-id="53873-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="53873-194">Os bits de 0 a 15 da marca propriedade indicam o tipo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="53873-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="53873-195">Os bits de 16 a 31 são o identificador da propriedade.</span><span class="sxs-lookup"><span data-stu-id="53873-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="53873-196">O tipo de propriedade determina como o restante da propriedade deve ser lido.</span><span class="sxs-lookup"><span data-stu-id="53873-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="53873-197">Valor Estático</span><span class="sxs-lookup"><span data-stu-id="53873-197">Static Value</span></span>

<span data-ttu-id="53873-198">Algumas propriedades não têm Dados de Valor e só têm dados na união.</span><span class="sxs-lookup"><span data-stu-id="53873-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="53873-199">Os seguintes tipos de propriedades (procedentes da Marca da Propriedade) devem interpretar os dados da União de Propriedade de 8 bytes da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="53873-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="53873-200">**Tipo de Propr**</span><span class="sxs-lookup"><span data-stu-id="53873-200">**Prop Type**</span></span>|<span data-ttu-id="53873-201">**Interpretação da União da Propriedade**</span><span class="sxs-lookup"><span data-stu-id="53873-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="53873-202">PT_I2</span></span>  <br/> |<span data-ttu-id="53873-203">short int</span><span class="sxs-lookup"><span data-stu-id="53873-203">short int rows</span></span>  <br/> |
|<span data-ttu-id="53873-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="53873-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="53873-205">long</span><span class="sxs-lookup"><span data-stu-id="53873-205">Long</span></span>  <br/> |
|<span data-ttu-id="53873-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="53873-206">PT_R4</span></span>  <br/> |<span data-ttu-id="53873-207">float</span><span class="sxs-lookup"><span data-stu-id="53873-207">float</span></span>  <br/> |
|<span data-ttu-id="53873-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="53873-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="53873-209">double</span><span class="sxs-lookup"><span data-stu-id="53873-209">double</span></span>  <br/> |
|<span data-ttu-id="53873-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="53873-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="53873-211">short int</span><span class="sxs-lookup"><span data-stu-id="53873-211">short int rows</span></span>  <br/> |
|<span data-ttu-id="53873-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="53873-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="53873-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="53873-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="53873-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="53873-214">PT_I8</span></span>  <br/> |<span data-ttu-id="53873-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="53873-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="53873-216">Valores Dinâmicos</span><span class="sxs-lookup"><span data-stu-id="53873-216">Dynamic Values</span></span>

<span data-ttu-id="53873-217">Outras propriedades têm dados em um bloco de Valor de Dados após os primeiros 16 bytes que contêm a Marca de Propriedade, os Dados Reservados e a União de Valor da Propriedade.</span><span class="sxs-lookup"><span data-stu-id="53873-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="53873-218">Ao contrário dos valores estáticos, os dados armazenados na União de Valor da Propriedade 8 bytes são irrelevantes para a leitura.</span><span class="sxs-lookup"><span data-stu-id="53873-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="53873-219">Ao gravar, certifique-se de preencher estes 8 bytes com algo.</span><span class="sxs-lookup"><span data-stu-id="53873-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="53873-220">No entanto, o conteúdo desses 8 bytes não é importante.</span><span class="sxs-lookup"><span data-stu-id="53873-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="53873-221">Nos valores dinâmicos, o tipo da marca de propriedade determina como interpretar os Dados de Valor.</span><span class="sxs-lookup"><span data-stu-id="53873-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="53873-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="53873-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="53873-223">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-223">**Value Data**</span></span>|<span data-ttu-id="53873-224">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-225">Número de bytes n</span><span class="sxs-lookup"><span data-stu-id="53873-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="53873-226">4</span><span class="sxs-lookup"><span data-stu-id="53873-226">-4</span></span>  <br/> |
|<span data-ttu-id="53873-227">Bytes a interpretar como uma cadeia de caracteres ANSI (inclui um terminador NULL)</span><span class="sxs-lookup"><span data-stu-id="53873-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="53873-228">n</span><span class="sxs-lookup"><span data-stu-id="53873-228">n</span></span>  <br/> |
   
<span data-ttu-id="53873-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="53873-229">PT_CLSID</span></span>
  
|<span data-ttu-id="53873-230">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-230">**Value Data**</span></span>|<span data-ttu-id="53873-231">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-232">Bytes a interpretar como um GUID</span><span class="sxs-lookup"><span data-stu-id="53873-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="53873-233">16</span><span class="sxs-lookup"><span data-stu-id="53873-233">-16</span></span>  <br/> |
|||
   
<span data-ttu-id="53873-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="53873-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="53873-235">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-235">**Value Data**</span></span>|<span data-ttu-id="53873-236">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-237">Número de bytes n</span><span class="sxs-lookup"><span data-stu-id="53873-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="53873-238">4</span><span class="sxs-lookup"><span data-stu-id="53873-238">-4</span></span>  <br/> |
|<span data-ttu-id="53873-239">Bytes a serem interpretados como uma matriz de byte</span><span class="sxs-lookup"><span data-stu-id="53873-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="53873-240">n</span><span class="sxs-lookup"><span data-stu-id="53873-240">n</span></span>  <br/> |
   
<span data-ttu-id="53873-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="53873-241">PT_ERROR</span></span>
  
|<span data-ttu-id="53873-242">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-242">**Value Data**</span></span>|<span data-ttu-id="53873-243">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-244">Número de bytes n</span><span class="sxs-lookup"><span data-stu-id="53873-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="53873-245">4</span><span class="sxs-lookup"><span data-stu-id="53873-245">-4</span></span>  <br/> |
|<span data-ttu-id="53873-246">Bytes a serem interpretados como uma matriz de byte</span><span class="sxs-lookup"><span data-stu-id="53873-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="53873-247">n</span><span class="sxs-lookup"><span data-stu-id="53873-247">n</span></span>  <br/> |
   
<span data-ttu-id="53873-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="53873-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="53873-249">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-249">**Value Data**</span></span>|<span data-ttu-id="53873-250">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-251">Número de matrizes binárias X</span><span class="sxs-lookup"><span data-stu-id="53873-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="53873-252">4</span><span class="sxs-lookup"><span data-stu-id="53873-252">-4</span></span>  <br/> |
|<span data-ttu-id="53873-253">Uma execução de bytes com X matrizes binárias.</span><span class="sxs-lookup"><span data-stu-id="53873-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="53873-254">Cada matriz deve ser interpretada exatamente como a execução de byte PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="53873-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="53873-255">Variável</span><span class="sxs-lookup"><span data-stu-id="53873-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="53873-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="53873-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="53873-257">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-257">**Value Data**</span></span>|<span data-ttu-id="53873-258">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-259">Número de cadeias de caracteres ANSI X</span><span class="sxs-lookup"><span data-stu-id="53873-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="53873-260">4</span><span class="sxs-lookup"><span data-stu-id="53873-260">-4</span></span>  <br/> |
|<span data-ttu-id="53873-261">Uma execução de bytes com X cadeias de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="53873-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="53873-262">Cada cadeia de caracteres deve ser interpretada exatamente como a execução de byte PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="53873-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="53873-263">Variável</span><span class="sxs-lookup"><span data-stu-id="53873-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="53873-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="53873-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="53873-265">**Dados do Valor**</span><span class="sxs-lookup"><span data-stu-id="53873-265">**Value Data**</span></span>|<span data-ttu-id="53873-266">**Número de Bytes**</span><span class="sxs-lookup"><span data-stu-id="53873-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53873-267">Número de cadeias de caracteres UNICODE X</span><span class="sxs-lookup"><span data-stu-id="53873-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="53873-268">4</span><span class="sxs-lookup"><span data-stu-id="53873-268">-4</span></span>  <br/> |
|<span data-ttu-id="53873-269">Uma execução de bytes que contém X cadeias de caracteres UNICODE.</span><span class="sxs-lookup"><span data-stu-id="53873-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="53873-270">Cada cadeia de caracteres deve ser interpretada exatamente como a execução de byte PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="53873-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="53873-271">Variável</span><span class="sxs-lookup"><span data-stu-id="53873-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="53873-272">Propriedades significativas</span><span class="sxs-lookup"><span data-stu-id="53873-272">Significant properties</span></span>

<span data-ttu-id="53873-273">Como mencionado anteriormente neste tópico, os blocos binários que representam propriedades têm marcas de propriedade que correspondem às propriedades nos destinatários de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="53873-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="53873-274">Para as propriedades que não estão listadas aqui, você pode pesquisar a descrição da propriedade na http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="53873-274">For properties that are not listed here, you can look up the property description at http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="53873-275">**Nome da propriedade**</span><span class="sxs-lookup"><span data-stu-id="53873-275">**Property Name**</span></span>|<span data-ttu-id="53873-276">**Marca de Propriedade**</span><span class="sxs-lookup"><span data-stu-id="53873-276">**Tag Property**</span></span>|<span data-ttu-id="53873-277">**Descrição (confira MSDN para saber mais)**</span><span class="sxs-lookup"><span data-stu-id="53873-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53873-278">PR_NICK_NAME_W (não transmitida aos destinatários, específica apenas para o fluxo de preenchimento automático)</span><span class="sxs-lookup"><span data-stu-id="53873-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="53873-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="53873-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="53873-280">Essa propriedade deve ser a primeira em cada linha de destinatário.</span><span class="sxs-lookup"><span data-stu-id="53873-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="53873-281">Serve funcionalmente como um importante identificador para a linha de destinatário.</span><span class="sxs-lookup"><span data-stu-id="53873-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="53873-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="53873-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="53873-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="53873-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="53873-284">O identificador de entrada de catálogo de endereço do destinatário.</span><span class="sxs-lookup"><span data-stu-id="53873-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="53873-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="53873-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="53873-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="53873-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="53873-287">O nome de exibição do destinatário.</span><span class="sxs-lookup"><span data-stu-id="53873-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="53873-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="53873-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="53873-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="53873-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="53873-290">O endereço de email do destinatário (por exemplo, joaosilva@contoso.com ou /o=Contoso/OU=Foo/cn=Recipients/cn=joaosilva)</span><span class="sxs-lookup"><span data-stu-id="53873-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="53873-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="53873-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="53873-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="53873-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="53873-293">O tipo de endereço do destinatário (por exemplo, SMTP ou EX).</span><span class="sxs-lookup"><span data-stu-id="53873-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="53873-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="53873-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="53873-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="53873-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="53873-296">A chave de pesquisa MAPI do destinatário.</span><span class="sxs-lookup"><span data-stu-id="53873-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="53873-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="53873-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="53873-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="53873-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="53873-299">O endereço SMTP do destinatário.</span><span class="sxs-lookup"><span data-stu-id="53873-299">The recipient's email address.</span></span>  <br/> |
|<span data-ttu-id="53873-300">PR_DROPDOWN_DISPLAY_NAME_W (não transmitida aos destinatários, específica apenas para o fluxo de preenchimento automático)</span><span class="sxs-lookup"><span data-stu-id="53873-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="53873-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="53873-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="53873-302">A cadeia de caracteres de exibição exibida na lista de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="53873-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="53873-303">PR_NICK_NAME_WEIGHT (não transmitida aos destinatários, específica apenas para o fluxo de preenchimento automático)</span><span class="sxs-lookup"><span data-stu-id="53873-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="53873-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="53873-304">0x60040003</span></span>  <br/> |<span data-ttu-id="53873-305">O peso desta entrada de preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="53873-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="53873-306">O peso é usado para determinar em que ordem ocorrem as entradas de preenchimento automático ao fazer a correspondência da lista preenchimento automático.</span><span class="sxs-lookup"><span data-stu-id="53873-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="53873-307">Entradas com maior peso são exibidas antes de entradas com peso inferior.</span><span class="sxs-lookup"><span data-stu-id="53873-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="53873-308">A lista completa de preenchimento automático é classificada por esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="53873-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="53873-309">O peso periodicamente diminui ao longo do tempo e aumenta quando o usuário envia um email para esse destinatário.</span><span class="sxs-lookup"><span data-stu-id="53873-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="53873-310">Confira a descrição neste tópico para saber mais sobre essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="53873-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="53873-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="53873-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="53873-312">O conjunto de linhas no fluxo de preenchimento automático é classificado em ordem decrescente pela propriedade PR_NICK_NAME_WEIGHT, e o fluxo de preenchimento automático sempre deve preservar esse característica de classificação.</span><span class="sxs-lookup"><span data-stu-id="53873-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="53873-313">Portanto, alterações ao peso da linha também devem garantir que a posição da linha mantém a ordem de classificação do conjunto completo de linhas.</span><span class="sxs-lookup"><span data-stu-id="53873-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="53873-314">Os acréscimos ao conjunto de linhas devem ser inseridos na posição correta para manter a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="53873-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="53873-315">O valor mínimo deste peso é de 0x1 e o valor máximo é LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="53873-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="53873-316">Outros valores de peso são considerados inválidos.</span><span class="sxs-lookup"><span data-stu-id="53873-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="53873-317">Quando o Outlook 2007 envia um email ou resolve um destinatário, ele aumenta o peso do destinatário em 0x2000.</span><span class="sxs-lookup"><span data-stu-id="53873-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

