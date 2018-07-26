---
title: Compatibilidade entre as versões de 32 bits e 64 bits do Office
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Descubra como a versão de 32 bits do Office é compatível com a versão de 64 bits do Office.
ms.openlocfilehash: 924f7a1aa891addc5841e6cdefc5226dcb056096
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771182"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a><span data-ttu-id="37355-103">Compatibilidade entre as versões de 32 bits e 64 bits do Office</span><span class="sxs-lookup"><span data-stu-id="37355-103">Compatibility Between the 32-bit and 64-bit Versions of Office</span></span>

<span data-ttu-id="37355-104">Descubra como a versão de 32 bits do Office é compatível com a versão de 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="37355-104">Find out how the 32-bit version of Office is compatible with the 64-bit version of Office.</span></span>
  
<span data-ttu-id="37355-105">Os aplicativos do Office estão disponíveis nas versões de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37355-105">Office applications are available in 32-bit and 64-bit versions.</span></span> 
  
<span data-ttu-id="37355-p101">As versões de 64 bits do Office permitem mover mais dados para aumentar a capacidade, por exemplo, quando você trabalha com números grandes no Microsoft Excel 2010. Ao escrever código de 32 bits, é possível usar a versão de 64 bits do Office sem qualquer alteração. No entanto, ao escrever código de 64 bits, você deverá garantir que ele contenha palavras-chave específicas e constantes de compilação condicional para garantir que o código tenha compatibilidade com a versão anterior do Office e que o código correto esteja sendo executado se você combinar os códigos de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37355-p101">The 64-bit versions of Office enable you to move more data around for increased capability, for example when you work with large numbers in Microsoft Excel 2010. When writing 32-bit code, you can use the 64-bit version of Office without any changes. However, when you write 64-bit code, you should ensure that your code contains specific keywords and conditional compilation constants to ensure that the code is backward compatible with earlier version of Office, and that the correct code is being executed if you mix 32-bit and 64-bit code.</span></span>
  
<span data-ttu-id="37355-p102">O Visual Basic for Applications 7.0 (VBA 7) é lançado nas versões de 64 bits para Office e funciona com aplicativos de 32 bits e 64 bits. As alterações descritas neste artigo aplicam-se apenas às versões de 64 bits do Office. Usar as versões de 32 bits do Microsoft Office permite usar soluções criadas em versões anteriores do Office sem modificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="37355-p102">Visual Basic for Applications 7.0 (VBA 7) is released in the 64-bit versions for Office, and it works with both 32-bit and 64-bit applications. The changes described in this article apply only to the 64-bit versions of Office. Using the 32-bit versions of Microsoft Office enable you to use solutions built in previous versions of Office without further modifications.</span></span>
  
> [!NOTE]
> <span data-ttu-id="37355-p103">Por padrão, quando você instala uma versão de 64 bits do Office, também instala a versão de 32 bits junto com o sistema de 64 bits. Você deve selecionar explicitamente a opção de instalação da versão de 64 bits do Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="37355-p103">By default, when you install a 64-bit version of Office, you also install the 32-bit version is installed along with the 64-bit system. You must explicitly select the Microsoft Office 64-bit version installation option.</span></span> 
  
<span data-ttu-id="37355-114">No VBA 7, você deve atualizar as instruções existentes da API do Windows (instruções **Declare**) para trabalhar com a versão de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37355-114">In VBA 7, you must update existing Windows API statements ( **Declare** statements) to work with the 64-bit version.</span></span> <span data-ttu-id="37355-115">Além disso, você deve atualizar os ponteiros de endereço e exibir alças de janela em tipos definidos pelo usuário que são usadas por estas instruções.</span><span class="sxs-lookup"><span data-stu-id="37355-115">Additionally, you must update address pointers and display window handles in user-defined types that are used by these statements.</span></span> <span data-ttu-id="37355-116">Isso é discutido mais detalhadamente neste artigo, bem como os problemas de compatibilidade entre as versões de 32 bits e 64 bits e as soluções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="37355-116">This is discussed in more detail in this article as well as compatibility issues between the 32-bit and 64-bit versions and suggested solutions.</span></span> 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a><span data-ttu-id="37355-117">Comparando os sistemas de 32 bits e 64 bits</span><span class="sxs-lookup"><span data-stu-id="37355-117">Comparing 32-bit and 64-bit systems</span></span>
<span data-ttu-id="37355-118"><a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a></span><span class="sxs-lookup"><span data-stu-id="37355-118"></span></span>

<span data-ttu-id="37355-p105">Os aplicativos criados com as versões de 64 bits do Office podem fazer referência a espaços de endereço maiores que as versões de 32 bits. Isso significa que é possível usar mais memória física para dados do que antes, possivelmente reduzindo a sobrecarga da movimentação de dados da memória física</span><span class="sxs-lookup"><span data-stu-id="37355-p105">Applications built with the 64-bit versions of Office can reference larger address spaces than 32-bit versions. This means you can use more physical memory for data than before, potentially reducing the overhead spent moving data in and out of physical memory</span></span>
  
<span data-ttu-id="37355-p106">Além de se referir a locais específicos (conhecidos como ponteiros) na memória física, você também pode usar endereços para fazer referência a identificadores de janela de exibição (conhecidos como alças). O tamanho (em bytes) do ponteiro ou alça depende se você estiver usando um sistema de 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37355-p106">In addition to referring specific locations (known as pointers) in physical memory, you can also use addresses to reference display window identifiers (known as handles). The size (in bytes) of the pointer or handle depends on whether you're using a 32-bit or 64-bit system.</span></span> 
  
<span data-ttu-id="37355-123">Se você desejar executar as soluções existentes com as versões de 64 bits do Office, lembre-se das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="37355-123">If you want to run your existing solutions with the 64-bit versions of Office, be aware of the following:</span></span>
  
- <span data-ttu-id="37355-p107">Os processos de 64 bits nativos no Office não podem carregar binários de 32 bits. Isso é um problema comum quando você tem controles do ActiveX da Microsoft e suplementos existentes.</span><span class="sxs-lookup"><span data-stu-id="37355-p107">Native 64-bit processes in Office cannot load 32-bit binaries. This is expected to be a common issue when you have existing Microsoft ActiveX controls and existing add-ins.</span></span>
    
- <span data-ttu-id="37355-p108">O VBA anteriormente não tinha um tipo de dados de ponteiro; portanto, você precisava usar variáveis de 32 bits para armazenar ponteiros e alças. Essas variáveis agora truncam valores de 64 bits retornados por chamadas de API ao usar instruções do **Declare**.</span><span class="sxs-lookup"><span data-stu-id="37355-p108">VBA previously didn't have a pointer data type, so you had to use 32-bit variables to store pointers and handles. These variables now truncate 64-bit values returned by API calls when using **Declare** statements.</span></span> 
    
## <a name="vba-7-code-base"></a><span data-ttu-id="37355-128">Base de código do VBA 7</span><span class="sxs-lookup"><span data-stu-id="37355-128">VBA 7 code base</span></span>
<span data-ttu-id="37355-129"><a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a></span><span class="sxs-lookup"><span data-stu-id="37355-129"></span></span>

<span data-ttu-id="37355-p109">O VBA 7 substitui a base de código do VBA no Office 2007 e em versões anteriores. O VBA 7 está disponível em ambas as versões de 32 bits e 64 bits do Office. Ele fornece duas constantes de compilação condicional:</span><span class="sxs-lookup"><span data-stu-id="37355-p109">VBA 7 replaces the VBA code base in Office 2007 and earlier versions. VBA 7 is available in both the 32-bit and 64-bit versions of Office. It provides two conditional compilation constants:</span></span> 
  
- <span data-ttu-id="37355-133">**VBA7** - Ajuda a garantir a compatibilidade com versões anteriores do seu código testando se seu aplicativo está usando o VBA 7 ou a versão anterior.</span><span class="sxs-lookup"><span data-stu-id="37355-133">**VBA7** - Helps ensure the backward compatibility of your code by testing whether your application is using VBA 7 or the previous version of VBA.</span></span> 
    
- <span data-ttu-id="37355-134">**Win64** - Testa se o código está sendo executado como 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37355-134">**Win64** Tests whether code is running as 32-bit or 64-bit.</span></span> 
    
<span data-ttu-id="37355-135">Com determinadas exceções, as macros em um documento que funcionam na versão de 32 bits do aplicativo também funcionam na versão de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="37355-135">With certain exceptions, the macros in a document that work in the 32-bit version of the application also work in the 64-bit version.</span></span>
  
## <a name="activex-control-and-com-add-in-compatibility"></a><span data-ttu-id="37355-136">Compatibilidade com controle ActiveX e suplemento de COM</span><span class="sxs-lookup"><span data-stu-id="37355-136">ActiveX control and COM add-in compatibility</span></span>
<span data-ttu-id="37355-137"><a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="37355-137"></span></span>

<span data-ttu-id="37355-p110">Os controles do ActiveX de 32 bits existentes não são compatíveis com as versões de 64 bits do Office. Para controles ActiveX e objetos COM:</span><span class="sxs-lookup"><span data-stu-id="37355-p110">Existing 32-bit ActiveX controls, are not compatible with the 64-bit versions of Office. For ActiveX controls and COM objects:</span></span>
  
- <span data-ttu-id="37355-140">Se você tiver o código-fonte, gere uma versão de 64 bits por conta própria.</span><span class="sxs-lookup"><span data-stu-id="37355-140">If you have the source code, generate a 64-bit version yourself.</span></span>
- <span data-ttu-id="37355-141">Se não tiver o código-fonte, peça uma versão atualizada ao fornecedor.</span><span class="sxs-lookup"><span data-stu-id="37355-141">If you don't have the source code, contact the vendor for an updated version.</span></span>
    
<span data-ttu-id="37355-p111">Os processos de 64 bits nativos no Office não podem carregar binários de 32 bits. Isso inclui os controles comuns de **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) e os controles de **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). Esses controles foram instalados pelas versões de 32 bits do Office anteriores ao Office 2010. Você precisará localizar uma alternativa para as soluções existentes do VBA que usam esses controles quando migrar o código para as versões de 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="37355-p111">Native 64-bit processes in Office cannot load 32-bit binaries. This includes the common controls of **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) and the controls of **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). These controls were installed by 32-bit versions of Office earlier than Office 2010. You'll need to find an alternative for your existing VBA solutions that use these controls when you migrate the code to the 64-bit versions of Office.</span></span> 
  
## <a name="api-compatibility"></a><span data-ttu-id="37355-146">Compatibilidade de API</span><span class="sxs-lookup"><span data-stu-id="37355-146">API compatibility</span></span>
<span data-ttu-id="37355-147"><a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a></span><span class="sxs-lookup"><span data-stu-id="37355-147"></span></span>

<span data-ttu-id="37355-p112">A combinação de VBA e das bibliotecas de tipo oferece diversas funcionalidades para criar aplicativos do Office. No entanto, às vezes, você deve se comunicar diretamente com o sistema operacional do computador e outros componentes, como quando você gerencia memória ou processos, ao trabalhar com elementos de interface de usuário como janelas e controles, ou ao modificar o registro do Windows. Nessas situações, sua melhor opção é usar uma das funções externas incorporados em arquivos DLL. Para fazer isso no VBA, faça chamadas de API usando instruções **Declare**.</span><span class="sxs-lookup"><span data-stu-id="37355-p112">The combination of VBA and type libraries gives you lots of functionality to create Office applications. However, sometimes you must communicate directly with the computer's operating system and other components, such as when you manage memory or processes, when working with UI elements linke windows and controls, or when modifying the Windows registry. In these scenarios, your best option is to use one of the external functions that are embedded in DLL files. You do this in VBA by making API calls using **Declare** statements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="37355-152">A Microsoft fornece um arquivo Win32API.txt que contém 1.500 instruções Declare e uma ferramenta para copiar a instrução **Declare** que você desejar para o seu código.</span><span class="sxs-lookup"><span data-stu-id="37355-152">Microsoft provides a Win32API.txt file that contains 1,500 Declare statements and a tool to copy the **Declare** statement that you want into your code.</span></span> <span data-ttu-id="37355-153">No entanto, essas instruções são para os sistemas de 32 bits e devem ser convertidas para 64 bits, usando as informações discutidas posteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="37355-153">However, these statements are for 32-bit systems and must be converted to 64-bit by using the information discussed later in this article.</span></span> <span data-ttu-id="37355-154">As instruções **Declare** existentes não compilarão no VBA de 64 bits até que tenham sido marcadas como seguras para 64 bits, usando o atributo **PtrSafe**.</span><span class="sxs-lookup"><span data-stu-id="37355-154">Existing **Declare** statements won't compile in 64-bit VBA until they've been marked as safe for 64-bit by using the **PtrSafe** attribute.</span></span> <span data-ttu-id="37355-155">Você pode localizar exemplos desse tipo de conversão no site de Jan Karel Pieterse, MVP de Excel: [http://www.jkp-ads.com/articles/apideclarations.asp](http://www.jkp-ads.com/articles/apideclarations.asp).</span><span class="sxs-lookup"><span data-stu-id="37355-155">You can find examples of this type of conversion at Excel MVP Jan Karel Pieterse's website at: [http://www.jkp-ads.com/articles/apideclarations.asp](http://www.jkp-ads.com/articles/apideclarations.asp).</span></span> <span data-ttu-id="37355-156">O [Guia do usuário do Inspetor de compatibilidade de código do Office](http://technet.microsoft.com/pt-BR/library/ee833946%28office.14%29.aspx) é uma ferramenta útil para inspecionar a sintaxe de instruções **Declare** da API do atributo **PtrSafe**, se necessário, e o tipo de retorno apropriado.</span><span class="sxs-lookup"><span data-stu-id="37355-156">> The [Office Code Compatibility Inspector user's guide](http://technet.microsoft.com/pt-BR/library/ee833946%28office.14%29.aspx) is a useful tool to inspect the syntax of API **Declare** statements for the **PtrSafe** attribute, if needed, and the appropriate return type.</span></span> 
  
<span data-ttu-id="37355-157">As instruções **Declare** são semelhantes ao seguinte, dependendo se você está chamando uma sub-rotina (que não tem valor de retorno) ou uma função (que tem um valor de retorno).</span><span class="sxs-lookup"><span data-stu-id="37355-157">**Declare** statements resemble one of the following, depending on whether you are calling a subroutine (which has no return value) or a function (which does have a return value).</span></span> 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

<span data-ttu-id="37355-p114">A função **SubName** ou **FunctionName** é substituída pelo nome real do procedimento no arquivo DLL e representa o nome usado quando o procedimento é chamado do código do VBA. Você também pode especificar um argumento **AliasName** para o nome do procedimento. O nome do arquivo DLL que contém o procedimento que está sendo chamado segue a palavra-chave **Lib**. E, finalmente, a lista de argumentos contém os parâmetros e os tipos de dados que devem ser passados ao procedimento.</span><span class="sxs-lookup"><span data-stu-id="37355-p114">The **SubName** function or **FunctionName** function is replaced by the actual name of the procedure in the DLL file and represents the name that is used when the procedure is called from VBA code. You can also specify an **AliasName** argument for the name of the procedure. The name of the DLL file that contains the procedure being called follows the **Lib** keyword. And finally, the argument list contains the parameters and the data types that must be passed to the procedure.</span></span> 
  
<span data-ttu-id="37355-162">A instrução seguinte **Declare** abre uma  *subchave*  no registro do Windows e substitui seu valor.</span><span class="sxs-lookup"><span data-stu-id="37355-162">The following **Declare** statement opens a  *subkey*  in the Windows registry and replaces its value.</span></span> 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

<span data-ttu-id="37355-163">A entrada Windows.h (alça da janela) para a função **RegOpenKeyA** é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="37355-163">The Windows.h (window handle) entry for the **RegOpenKeyA** function is as follows:</span></span> 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

<span data-ttu-id="37355-p115">No Visual C e no Microsoft Visual C++, o exemplo anterior compila corretamente para 32 bits e 64 bits. Isso ocorre porque HKEY está definida como um ponteiro cujo tamanho reflete o tamanho da memória da plataforma na qual o código é compilado.</span><span class="sxs-lookup"><span data-stu-id="37355-p115">In Visual C and Microsoft Visual C++, the previous example compiles correctly for both 32-bit and 64-bit. This is because HKEY is defined as a pointer, whose size reflects the memory size of the platform that the code is compiled in.</span></span>
  
<span data-ttu-id="37355-p116">Em versões anteriores do VBA, não havia nenhum tipo de dados de ponteiro específico de modo que o tipo de dados **Long** era usado. E como o tipo de dados **Long** sempre é 32 bits, ocorre falha quando é usado em um sistema com memória de 64 bits, porque os 32 bits de cima podem ser truncados ou podem substituir outros endereços de memória. Cada uma destas situações pode resultar em comportamentos imprevisíveis ou falhas de sistema.</span><span class="sxs-lookup"><span data-stu-id="37355-p116">In previous versions of VBA, there was no specific pointer data type so the **Long** data type was used. And because the **Long** data type is always 32-bits, this breaks when used on a system with 64-bit memory because the upper 32-bits might be truncated or might overwrite other memory addresses. Either of these situations can result in unpredictable behavior or system crashes.</span></span> 
  
<span data-ttu-id="37355-p117">Para resolver isso, o VBA inclui um tipo de dados de  *ponteiro*  verdadeiro: **LongPtr**. Esse novo tipo de dados permite que você escreva a instrução **Declare** original corretamente da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="37355-p117">To resolve this, VBA includes a true  *pointer*  data type: **LongPtr**. This new data type enables you to write the original **Declare** statement correctly as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

<span data-ttu-id="37355-p118">Esse tipo de dados e o novo atributo **PtrSafe** permitem que você use esta instrução **Declare** em sistemas de 32 bits ou 64 bits. O atributo **PtrSafe** indica para o compilador de VBA que a instrução **Declare** está direcionada para a versão de 64 bits do Office. Sem esse atributo, usar a instrução **Declare** em um sistema de 64 bits resultará em um erro em tempo de compilação. O atributo **PtrSafe** é opcional na versão de 32 bits do Office. Isso permite que instruções **Declare** existentes funcionem como de costume.</span><span class="sxs-lookup"><span data-stu-id="37355-p118">This data type and the new **PtrSafe** attribute enable you to use this **Declare** statement on either 32-bit or 64-bit systems. The **PtrSafe** attribute indicates to the VBA compiler that the **Declare** statement is targeted for the 64-bit version of Office. Without this attribute, using the **Declare** statement in a 64-bit system will result in a compile-time error. The **PtrSafe** attribute is optional on the 32-bit version of Office. This enables existing **Declare** statements to work as they always have.</span></span> 
  
<span data-ttu-id="37355-176">A tabela a seguir fornece mais informações sobre o novo qualificador e os tipos de dados bem como outro tipo de dados, dois operadores de conversão e três funções.</span><span class="sxs-lookup"><span data-stu-id="37355-176">The following table provides more information about the new qualifier and data typeas well as another data type, two conversion operators, and three functions.</span></span>
  
|<span data-ttu-id="37355-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="37355-177">Type</span></span>|<span data-ttu-id="37355-178">Item</span><span class="sxs-lookup"><span data-stu-id="37355-178">Item</span></span>|<span data-ttu-id="37355-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="37355-179">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37355-180">Qualificador</span><span class="sxs-lookup"><span data-stu-id="37355-180">Qualifier</span></span>  <br/> |<span data-ttu-id="37355-181">**PtrSafe**</span><span class="sxs-lookup"><span data-stu-id="37355-181">**PtrSafe**</span></span> <br/> |<span data-ttu-id="37355-p119">Indica que a instrução **Declare** é compatível com 64 bits. Esse atributo é obrigatório em sistemas de 64 bits.  </span><span class="sxs-lookup"><span data-stu-id="37355-p119">Indicates that the **Declare** statement is compatible with 64-bits. This attribute is mandatory on 64-bit systems.  </span></span><br/> |
|<span data-ttu-id="37355-184">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="37355-184">Data Type</span></span>  <br/> |<span data-ttu-id="37355-185">**LongPtr**</span><span class="sxs-lookup"><span data-stu-id="37355-185">**LongPtr**</span></span> <br/> |<span data-ttu-id="37355-p120">Um tipo de dados da variável que é um tipo de dados de 4 bytes em versões de 32 bits e um tipo de dados de 8 bytes em versões de 64 bits do Microsoft Office. Essa é a maneira recomendada de declarar um ponteiro ou uma alça do novo código, mas também para código herdado se ele tiver para executar a versão de 64 bits do Office. Só é suportado no tempo de execução do VBA 7 de 32 bits e 64 bits. Você pode atribuir valores numéricos a ele, mas não tipos numéricos.</span><span class="sxs-lookup"><span data-stu-id="37355-p120">A variable data type which is a 4-bytes data type on 32-bit versions and an 8-byte data type on 64-bit versions of Microsoft Office. This is the recommended way of declaring a pointer or a handle for new code but also for legacy code if it has to run in the 64-bit version of Office. It is only supported in the VBA 7 runtime on 32-bit and 64-bit. Note that you can assign numeric values to it but not numeric types.</span></span>  <br/> |
|<span data-ttu-id="37355-190">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="37355-190">Data Type</span></span>  <br/> |<span data-ttu-id="37355-191">**LongLong**</span><span class="sxs-lookup"><span data-stu-id="37355-191">**LongLong**</span></span> <br/> |<span data-ttu-id="37355-p121">Esse é um tipo de dados de 8 bytes que está disponível somente em versões de 64 bits do Microsoft Office. Você pode atribuir valores numéricos, mas não tipos numéricos (para evitar truncamento).</span><span class="sxs-lookup"><span data-stu-id="37355-p121">This is an 8-byte data type which is available only in 64-bit versions of Microsoft Office. You can assign numeric values but not numeric types (to avoid truncation).</span></span>  <br/> |
|<span data-ttu-id="37355-194">Operador de conversão</span><span class="sxs-lookup"><span data-stu-id="37355-194">Conversion Operator</span></span>  <br/> |<span data-ttu-id="37355-195">**CLngPtr**</span><span class="sxs-lookup"><span data-stu-id="37355-195">**CLngPtr**</span></span> <br/> |<span data-ttu-id="37355-196">Converte uma expressão simples em um tipo de dados **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="37355-196">Converts a simple expression to a **LongPtr** data type.</span></span>  <br/> |
|<span data-ttu-id="37355-197">Operador de conversão</span><span class="sxs-lookup"><span data-stu-id="37355-197">Conversion Operator</span></span>  <br/> |<span data-ttu-id="37355-198">**CLngLng**</span><span class="sxs-lookup"><span data-stu-id="37355-198">**CLngLng**</span></span> <br/> |<span data-ttu-id="37355-199">Converte uma expressão simples em um tipo de dados **LongLong**.</span><span class="sxs-lookup"><span data-stu-id="37355-199">Converts a simple expression to a **LongLong** data type.</span></span>  <br/> |
|<span data-ttu-id="37355-200">Função</span><span class="sxs-lookup"><span data-stu-id="37355-200">Function</span></span>  <br/> |<span data-ttu-id="37355-201">**VarPtr**</span><span class="sxs-lookup"><span data-stu-id="37355-201">**VarPtr**</span></span> <br/> |<span data-ttu-id="37355-p122">Conversor variante. Retorna um **LongPtr** em versões de 64 bits e um **Long** em versões de 32 bits (4 bytes).  </span><span class="sxs-lookup"><span data-stu-id="37355-p122">Variant converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="37355-204">Função</span><span class="sxs-lookup"><span data-stu-id="37355-204">Function</span></span>  <br/> |<span data-ttu-id="37355-205">**ObjPtr**</span><span class="sxs-lookup"><span data-stu-id="37355-205">**ObjPtr**</span></span> <br/> |<span data-ttu-id="37355-p123">Conversor de objeto. Retorna um **LongPtr** em versões de 64 bits e um **Long** em versões de 32 bits (4 bytes).  </span><span class="sxs-lookup"><span data-stu-id="37355-p123">Object converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
|<span data-ttu-id="37355-208">Função</span><span class="sxs-lookup"><span data-stu-id="37355-208">Function</span></span>  <br/> |<span data-ttu-id="37355-209">**StrPtr**</span><span class="sxs-lookup"><span data-stu-id="37355-209">**StrPtr**</span></span> <br/> |<span data-ttu-id="37355-p124">Conversor de cadeia de caracteres. Retorna um **LongPtr** em versões de 64 bits e um **Long** em versões de 32 bits (4 bytes).  </span><span class="sxs-lookup"><span data-stu-id="37355-p124">String converter. Returns a **LongPtr** on 64-bit versions, and a **Long** on 32-bit versions (4 bytes).  </span></span><br/> |
   
<span data-ttu-id="37355-212">O exemplo a seguir mostra como usar alguns desses itens em uma instrução **Declare**.</span><span class="sxs-lookup"><span data-stu-id="37355-212">The follow example shows how to use some of these items in a **Declare** statement.</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

<span data-ttu-id="37355-213">As instruções **Declare** sem o atributo **PtrSafe** são consideradas não compatíveis com a versão de 64 bits do Office.</span><span class="sxs-lookup"><span data-stu-id="37355-213">Note that **Declare** statements without the **PtrSafe** attribute are assumed not to be compatible with the 64-bit version of Office.</span></span> 
  
<span data-ttu-id="37355-p125">Há duas constantes de compilação condicional: **VBA7** e **Win64**. Para garantir a compatibilidade com versões anteriores do Microsoft Office, você usa a constante **VBA7** (esse é o caso mais comum) para impedir o código de 64 bits de ser usado na versão anterior do Office. Para código que é diferente entre a versão de 32 bits e a de 64 bits, como chamar uma API matemática que usa **LongLong** para sua versão de 64 bits e **Long** para sua versão de 32 bits, você usa a constante **Win64**. O código a seguir mostra o uso de duas dessas constantes.</span><span class="sxs-lookup"><span data-stu-id="37355-p125">There are two conditional compilation constants: **VBA7** and **Win64**. To ensure backward compatibility with previous versions of Microsoft Office, you use the **VBA7** constant (this is the more typical case) to prevent 64-bit code from being used in the earlier version of Office. For code that is different between the 32-bit version and the 64-bit version, such as calling a math API that uses **LongLong** for its 64-bit version and **Long** for its 32-bit version, you use the **Win64** constant. The following code shows the use of these two constants.</span></span> 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

<span data-ttu-id="37355-p126">Para resumir, se você escreve código de 64 bits e pretende usá-lo em versões anteriores do Office, convém usar a constante de compilação condicional **VBA7**. No entanto, se você escrever código de 32 bits no Office, esse código funcionará como nas versões anteriores do Office sem a necessidade da constante de compilação. Se você deseja garantir que está usando instruções de 32 bits para versões de 32 bits e instruções de 64 bits para versões de 64 bits, a melhor opção é usar a constante de compilação condicional **Win64**.</span><span class="sxs-lookup"><span data-stu-id="37355-p126">To summarize, if you write 64-bit code and intend to use it in previous versions of Office, you will want to use the **VBA7** conditional compilation constant. However, if you write 32-bit code in Office, that code works as is in previous versions of Office without the need for the compilation constant. If you want to ensure that you are using 32-bit statements for 32-bit versions and 64-bit statements for 64-bit versions, your best option is to use the **Win64** conditional compilation constant.</span></span> 
  
## <a name="using-conditional-compilation-attributes"></a><span data-ttu-id="37355-221">Usar atributos de compilação condicional</span><span class="sxs-lookup"><span data-stu-id="37355-221">Using Conditional Compilation Attributes</span></span>
<span data-ttu-id="37355-222"><a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a></span><span class="sxs-lookup"><span data-stu-id="37355-222"></span></span>

<span data-ttu-id="37355-p127">O exemplo a seguir mostra o código VBA escrito para 32 bits que precisa ser atualizado. Observe os tipos de dados no código legado que são atualizados para usar **LongPtr** porque se referem a identificadores ou ponteiros.</span><span class="sxs-lookup"><span data-stu-id="37355-p127">The following example shows VBA code written for 32-bit that needs to be updated. Notice the data types in the legacy code that are updated to use **LongPtr** because they refer to handles or pointers.</span></span> 
  
### <a name="vba-code-written-for-32-bit-versions"></a><span data-ttu-id="37355-225">Código VBA escrito para versões de 32 bits</span><span class="sxs-lookup"><span data-stu-id="37355-225">VBA code written for 32-bit versions</span></span>
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a><span data-ttu-id="37355-226">Código VBA reescrito para versões de 64 bits</span><span class="sxs-lookup"><span data-stu-id="37355-226">VBA code rewritten for 64-bit versions</span></span>
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<span data-ttu-id="37355-227"><a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a></span><span class="sxs-lookup"><span data-stu-id="37355-227"></span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="37355-228">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="37355-228">Frequently asked questions</span></span>

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a><span data-ttu-id="37355-229">Quando devo usar a versão de 64 bits do Office?</span><span class="sxs-lookup"><span data-stu-id="37355-229">When should I use the 64-bit version of Office?</span></span>
  
<span data-ttu-id="37355-p128">Isso é mais uma questão de qual aplicativo host (Excel, Word e assim por diante) você está usando. Por exemplo, o Excel é capaz de manipular planilhas muito maiores com a versão de 64 bits do Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="37355-p128">This is more a matter of which host application (Excel, Word, and so forth) you are using. For example, Excel is able to handle much larger worksheets with the 64-bit version of Microsoft Office.</span></span>
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a><span data-ttu-id="37355-232">Posso instalar versões de 32 bits e 64 bits do Office lado a lado?</span><span class="sxs-lookup"><span data-stu-id="37355-232">Can I install 64-bit and 32-bit versions of Office side-by-side?</span></span>
  
<span data-ttu-id="37355-233">Não.</span><span class="sxs-lookup"><span data-stu-id="37355-233">No.</span></span>
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a><span data-ttu-id="37355-234">Quando devo converter parâmetros de Long para LongPtr?</span><span class="sxs-lookup"><span data-stu-id="37355-234">When should I convert Long parameters to LongPtr?</span></span>
  
<span data-ttu-id="37355-p129">Você precisa verificar a documentação da API do Windows na rede de desenvolvedores da Microsoft para a função que deseja chamar. Ponteiros e alças precisam ser convertidos para **LongPtr**. Por exemplo, a documentação para [RegOpenKeyA](http://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) fornece a assinatura a seguir:</span><span class="sxs-lookup"><span data-stu-id="37355-p129">You need to check the Windows API documentation on the Microsoft Developers Network for the function you want to call. Handles and pointers need to be converted to **LongPtr**. As an example, the documentation for [RegOpenKeyA](http://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) provides the following signature:</span></span> 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

<span data-ttu-id="37355-238">Os parâmetros são definidos como:</span><span class="sxs-lookup"><span data-stu-id="37355-238">The parameters are defined as:</span></span>
  
|<span data-ttu-id="37355-239">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="37355-239">Parameter</span></span>|<span data-ttu-id="37355-240">Descrição</span><span class="sxs-lookup"><span data-stu-id="37355-240">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="37355-241">hKey [in]</span><span class="sxs-lookup"><span data-stu-id="37355-241">hKey [in]</span></span>  <br/> |<span data-ttu-id="37355-242">Uma  *alça*  para uma chave do Registro aberta.</span><span class="sxs-lookup"><span data-stu-id="37355-242">A  *handle*  to an open registry key.</span></span>  <br/> |
|<span data-ttu-id="37355-243">lpSubKey [in, optional]</span><span class="sxs-lookup"><span data-stu-id="37355-243">lpSubKey [in, optional]</span></span>  <br/> |<span data-ttu-id="37355-244">O nome da subchave de registro a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="37355-244">The name of the registry subkey to be opened.</span></span>  <br/> |
|<span data-ttu-id="37355-245">ulOptions</span><span class="sxs-lookup"><span data-stu-id="37355-245">ulOptions</span></span>  <br/> |<span data-ttu-id="37355-246">Esse parâmetro está reservado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="37355-246">This parameter is reserved and must be zero.</span></span>  <br/> |
|<span data-ttu-id="37355-247">samDesired [in]</span><span class="sxs-lookup"><span data-stu-id="37355-247">samDesired [in]</span></span>  <br/> |<span data-ttu-id="37355-248">Uma máscara que especifica os direitos de acesso desejado para a chave.</span><span class="sxs-lookup"><span data-stu-id="37355-248">A mask that specifies the desired access rights to the key.</span></span>  <br/> |
|<span data-ttu-id="37355-249">phkResult [out]</span><span class="sxs-lookup"><span data-stu-id="37355-249">phkResult [out]</span></span>  <br/> |<span data-ttu-id="37355-250">Um  *ponteiro*  para uma variável que recebe uma alça para a chave aberta.</span><span class="sxs-lookup"><span data-stu-id="37355-250">A  *pointer*  to a variable that receives a handle to the opened key.</span></span>  <br/> |
   
<span data-ttu-id="37355-251">No [Win32API_PtrSafe.txt](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), a instrução **Declare** é definida como:</span><span class="sxs-lookup"><span data-stu-id="37355-251">In [Win32API_PtrSafe.txt](http://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), the **Declare** statement is defined as:</span></span> 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a><span data-ttu-id="37355-252">Posso converter ponteiros e alças em estruturas?</span><span class="sxs-lookup"><span data-stu-id="37355-252">Should I convert pointers and handles in structures?</span></span>
  
<span data-ttu-id="37355-p130">Sim. Confira o tipo **MSG** em Win32API_PtrSafe.txt:</span><span class="sxs-lookup"><span data-stu-id="37355-p130">Yes. See the **MSG** type in Win32API_PtrSafe.txt:</span></span> 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a><span data-ttu-id="37355-255">Quando devo usar strptr varpt e objptr?</span><span class="sxs-lookup"><span data-stu-id="37355-255">When should I use strptr, varpt, and objptr?</span></span>
  
<span data-ttu-id="37355-p131">Você deve usar essas funções para recuperar ponteiros para cadeias de caracteres, variáveis e objetos, respectivamente. Na versão de 64 bits do Office, essas funções retornarão um **LongPtr** de 64 bits, que pode ser passado para instruções **Declare**. O uso dessas funções não mudou de versões anteriores do VBA. A única diferença é que elas agora retornam um **LongPtr**.</span><span class="sxs-lookup"><span data-stu-id="37355-p131">You should use these functions to retrieve pointers to strings, variables and objects, respectively. On the 64-bit version of Office, these functions will return a 64-bit **LongPtr**, which can be passed to **Declare** statements. The use of these functions has not changed from previous versions of VBA. The only difference is that they now return a **LongPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="37355-260">Confira também</span><span class="sxs-lookup"><span data-stu-id="37355-260">See also</span></span>
<span data-ttu-id="37355-261"><a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a></span><span class="sxs-lookup"><span data-stu-id="37355-261"></span></span>

- [<span data-ttu-id="37355-262">Anatomy of a Declare Statement</span><span class="sxs-lookup"><span data-stu-id="37355-262">Anatomy of a Declare Statement</span></span>](https://msdn.microsoft.com/pt-BR/library/office/aa671659.aspx)
    

