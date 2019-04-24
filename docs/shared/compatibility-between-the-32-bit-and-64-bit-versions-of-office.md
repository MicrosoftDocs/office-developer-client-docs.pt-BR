---
title: Compatibilidade entre as versões de 32 bits e 64 bits do Office
ms.date: 04/27/2016
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Descubra como a versão de 32 bits do Office é compatível com a versão de 64 bits do Office.
localization_priority: Priority
ms.openlocfilehash: b03323b37b242c9992c47cd737ae54f3f9bbf2ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359819"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Compatibilidade entre as versões de 32 bits e 64 bits do Office

Descubra como a versão de 32 bits do Office é compatível com a versão de 64 bits do Office.
  
Os aplicativos do Office estão disponíveis nas versões de 32 e 64 bits. 
  
As versões de 64 bits do Office permitem mover mais dados para aumentar a capacidade, por exemplo, quando você trabalha com números grandes no Microsoft Excel 2010. Ao escrever código de 32 bits, é possível usar a versão de 64 bits do Office sem qualquer alteração. No entanto, ao escrever código de 64 bits, você deverá garantir que ele contenha palavras-chave específicas e constantes de compilação condicional para garantir que o código tenha compatibilidade com a versão anterior do Office e que o código correto esteja sendo executado se você combinar os códigos de 32 bits e 64 bits.
  
O Visual Basic for Applications 7.0 (VBA 7) é lançado nas versões de 64 bits para Office e funciona com aplicativos de 32 bits e 64 bits. As alterações descritas neste artigo aplicam-se apenas às versões de 64 bits do Office. Usar as versões de 32 bits do Microsoft Office permite usar soluções criadas em versões anteriores do Office sem modificações adicionais.
  
> [!NOTE]
> Por padrão, quando você instala uma versão de 64 bits do Office, também instala a versão de 32 bits junto com o sistema de 64 bits. Você deve selecionar explicitamente a opção de instalação da versão de 64 bits do Microsoft Office. 
  
No VBA 7, você deve atualizar as instruções existentes da API do Windows (instruções **Declare**) para trabalhar com a versão de 64 bits. Além disso, você deve atualizar os ponteiros de endereço e exibir alças de janela em tipos definidos pelo usuário que são usadas por estas instruções. Isso é discutido mais detalhadamente neste artigo, bem como os problemas de compatibilidade entre as versões de 32 bits e 64 bits e as soluções sugeridas. 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>Comparando os sistemas de 32 bits e 64 bits
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

Os aplicativos criados com as versões de 64 bits do Office podem fazer referência a espaços de endereço maiores que as versões de 32 bits. Isso significa que é possível usar mais memória física para dados do que antes, possivelmente reduzindo a sobrecarga da movimentação de dados da memória física
  
Além de se referir a locais específicos (conhecidos como ponteiros) na memória física, você também pode usar endereços para fazer referência a identificadores de janela de exibição (conhecidos como alças). O tamanho (em bytes) do ponteiro ou alça depende se você estiver usando um sistema de 32 bits ou 64 bits. 
  
Se você desejar executar as soluções existentes com as versões de 64 bits do Office, lembre-se das seguintes opções:
  
- Os processos de 64 bits nativos no Office não podem carregar binários de 32 bits. Isso é um problema comum quando você tem controles do ActiveX da Microsoft e suplementos existentes.
    
- O VBA anteriormente não tinha um tipo de dados de ponteiro; portanto, você precisava usar variáveis de 32 bits para armazenar ponteiros e alças. Essas variáveis agora truncam valores de 64 bits retornados por chamadas de API ao usar instruções do **Declare**. 
    
## <a name="vba-7-code-base"></a>Base de código do VBA 7
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

O VBA 7 substitui a base de código do VBA no Office 2007 e em versões anteriores. O VBA 7 está disponível em ambas as versões de 32 bits e 64 bits do Office. Ele fornece duas constantes de compilação condicional: 
  
- **VBA7** - Ajuda a garantir a compatibilidade com versões anteriores do seu código testando se seu aplicativo está usando o VBA 7 ou a versão anterior. 
    
- **Win64** - Testa se o código está sendo executado como 32 bits ou 64 bits. 
    
Com determinadas exceções, as macros em um documento que funcionam na versão de 32 bits do aplicativo também funcionam na versão de 64 bits.
  
## <a name="activex-control-and-com-add-in-compatibility"></a>Compatibilidade com controle ActiveX e suplemento de COM
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

Os controles do ActiveX de 32 bits existentes não são compatíveis com as versões de 64 bits do Office. Para controles ActiveX e objetos COM:
  
- Se você tiver o código-fonte, gere uma versão de 64 bits por conta própria.
- Se não tiver o código-fonte, peça uma versão atualizada ao fornecedor.
    
Os processos de 64 bits nativos no Office não podem carregar binários de 32 bits. Isso inclui os controles comuns de **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) e os controles de **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). Esses controles foram instalados pelas versões de 32 bits do Office anteriores ao Office 2010. Você precisará localizar uma alternativa para as soluções existentes do VBA que usam esses controles quando migrar o código para as versões de 64 bits do Office. 
  
## <a name="api-compatibility"></a>Compatibilidade de API
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

A combinação de VBA e das bibliotecas de tipo oferece diversas funcionalidades para criar aplicativos do Office. No entanto, às vezes, você deve se comunicar diretamente com o sistema operacional do computador e outros componentes, como quando você gerencia memória ou processos, ao trabalhar com elementos de interface de usuário como janelas e controles, ou ao modificar o registro do Windows. Nessas situações, sua melhor opção é usar uma das funções externas incorporados em arquivos DLL. Para fazer isso no VBA, faça chamadas de API usando instruções **Declare**. 
  
> [!NOTE]
> A Microsoft fornece um arquivo Win32API.txt que contém 1.500 instruções Declare e uma ferramenta para copiar a instrução **Declare** que você desejar para o seu código. No entanto, essas instruções são para os sistemas de 32 bits e devem ser convertidas para 64 bits, usando as informações discutidas posteriormente neste artigo. As instruções **Declare** existentes não compilarão no VBA de 64 bits até que tenham sido marcadas como seguras para 64 bits, usando o atributo **PtrSafe**. Você pode localizar exemplos desse tipo de conversão no site de Jan Karel Pieterse, MVP de Excel: [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp). O [Guia do usuário do Inspetor de compatibilidade de código do Office](https://technet.microsoft.com/pt-BR/library/ee833946%28office.14%29.aspx) é uma ferramenta útil para inspecionar a sintaxe de instruções **Declare** da API do atributo **PtrSafe**, se necessário, e o tipo de retorno apropriado. 
  
As instruções **Declare** são semelhantes ao seguinte, dependendo se você está chamando uma sub-rotina (que não tem valor de retorno) ou uma função (que tem um valor de retorno). 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

A função **SubName** ou **FunctionName** é substituída pelo nome real do procedimento no arquivo DLL e representa o nome usado quando o procedimento é chamado do código do VBA. Você também pode especificar um argumento **AliasName** para o nome do procedimento. O nome do arquivo DLL que contém o procedimento que está sendo chamado segue a palavra-chave **Lib**. E, finalmente, a lista de argumentos contém os parâmetros e os tipos de dados que devem ser passados ao procedimento. 
  
A instrução seguinte **Declare** abre uma  *subchave*  no registro do Windows e substitui seu valor. 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

A entrada Windows.h (alça da janela) para a função **RegOpenKeyA** é a seguinte: 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

No Visual C e no Microsoft Visual C++, o exemplo anterior compila corretamente para 32 bits e 64 bits. Isso ocorre porque HKEY está definida como um ponteiro cujo tamanho reflete o tamanho da memória da plataforma na qual o código é compilado.
  
Em versões anteriores do VBA, não havia nenhum tipo de dados de ponteiro específico de modo que o tipo de dados **Long** era usado. E como o tipo de dados **Long** sempre é 32 bits, ocorre falha quando é usado em um sistema com memória de 64 bits, porque os 32 bits de cima podem ser truncados ou podem substituir outros endereços de memória. Cada uma destas situações pode resultar em comportamentos imprevisíveis ou falhas de sistema. 
  
Para resolver isso, o VBA inclui um tipo de dados de  *ponteiro*  verdadeiro: **LongPtr**. Esse novo tipo de dados permite que você escreva a instrução **Declare** original corretamente da seguinte maneira: 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

Esse tipo de dados e o novo atributo **PtrSafe** permitem que você use esta instrução **Declare** em sistemas de 32 bits ou 64 bits. O atributo **PtrSafe** indica para o compilador de VBA que a instrução **Declare** está direcionada para a versão de 64 bits do Office. Sem esse atributo, usar a instrução **Declare** em um sistema de 64 bits resultará em um erro em tempo de compilação. O atributo **PtrSafe** é opcional na versão de 32 bits do Office. Isso permite que instruções **Declare** existentes funcionem como de costume. 
  
A tabela a seguir fornece mais informações sobre o novo qualificador e os tipos de dados bem como outro tipo de dados, dois operadores de conversão e três funções.
  
|Tipo|Item|Descrição|
|:-----|:-----|:-----|
|Qualificador  <br/> |**PtrSafe** <br/> |Indica que a instrução **Declare** é compatível com 64 bits. Esse atributo é obrigatório em sistemas de 64 bits.  <br/> |
|Tipo de dados  <br/> |**LongPtr** <br/> |Um tipo de dados da variável que é um tipo de dados de 4 bytes em versões de 32 bits e um tipo de dados de 8 bytes em versões de 64 bits do Microsoft Office. Essa é a maneira recomendada de declarar um ponteiro ou uma alça do novo código, mas também para código herdado se ele tiver para executar a versão de 64 bits do Office. Só é suportado no tempo de execução do VBA 7 de 32 bits e 64 bits. Você pode atribuir valores numéricos a ele, mas não tipos numéricos.  <br/> |
|Tipo de dados  <br/> |**LongLong** <br/> |Esse é um tipo de dados de 8 bytes que está disponível somente em versões de 64 bits do Microsoft Office. Você pode atribuir valores numéricos, mas não tipos numéricos (para evitar truncamento).  <br/> |
|Operador de conversão  <br/> |**CLngPtr** <br/> |Converte uma expressão simples em um tipo de dados **LongPtr**.  <br/> |
|Operador de conversão  <br/> |**CLngLng** <br/> |Converte uma expressão simples em um tipo de dados **LongLong**.  <br/> |
|Função  <br/> |**VarPtr** <br/> |Conversor variante. Retorna um **LongPtr** em versões de 64 bits e um **Long** em versões de 32 bits (4 bytes).  <br/> |
|Função  <br/> |**ObjPtr** <br/> |Conversor de objeto. Retorna um **LongPtr** em versões de 64 bits e um **Long** em versões de 32 bits (4 bytes).  <br/> |
|Função  <br/> |**StrPtr** <br/> |Conversor de cadeia de caracteres. Retorna um **LongPtr** em versões de 64 bits e um **Long** em versões de 32 bits (4 bytes).  <br/> |
   
O exemplo a seguir mostra como usar alguns desses itens em uma instrução **Declare**. 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

As instruções **Declare** sem o atributo **PtrSafe** são consideradas não compatíveis com a versão de 64 bits do Office. 
  
Há duas constantes de compilação condicional: **VBA7** e **Win64**. Para garantir a compatibilidade com versões anteriores do Microsoft Office, você usa a constante **VBA7** (esse é o caso mais comum) para impedir o código de 64 bits de ser usado na versão anterior do Office. Para código que é diferente entre a versão de 32 bits e a de 64 bits, como chamar uma API matemática que usa **LongLong** para sua versão de 64 bits e **Long** para sua versão de 32 bits, você usa a constante **Win64**. O código a seguir mostra o uso de duas dessas constantes. 
  
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

Para resumir, se você escreve código de 64 bits e pretende usá-lo em versões anteriores do Office, convém usar a constante de compilação condicional **VBA7**. No entanto, se você escrever código de 32 bits no Office, esse código funcionará como nas versões anteriores do Office sem a necessidade da constante de compilação. Se você deseja garantir que está usando instruções de 32 bits para versões de 32 bits e instruções de 64 bits para versões de 64 bits, a melhor opção é usar a constante de compilação condicional **Win64**. 
  
## <a name="using-conditional-compilation-attributes"></a>Usar atributos de compilação condicional
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

O exemplo a seguir mostra o código VBA escrito para 32 bits que precisa ser atualizado. Observe os tipos de dados no código legado que são atualizados para usar **LongPtr** porque se referem a identificadores ou ponteiros. 
  
### <a name="vba-code-written-for-32-bit-versions"></a>Código VBA escrito para versões de 32 bits
  
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

### <a name="vba-code-rewritten-for-64-bit-versions"></a>Código VBA reescrito para versões de 64 bits
  
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

<a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a>

## <a name="frequently-asked-questions"></a>Perguntas frequentes

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a>Quando devo usar a versão de 64 bits do Office?
  
Isso é mais uma questão de qual aplicativo host (Excel, Word e assim por diante) você está usando. Por exemplo, o Excel é capaz de manipular planilhas muito maiores com a versão de 64 bits do Microsoft Office.
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>Posso instalar versões de 32 bits e 64 bits do Office lado a lado?
  
Não.
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>Quando devo converter parâmetros de Long para LongPtr?
  
Você precisa verificar a documentação da API do Windows na rede de desenvolvedores da Microsoft para a função que deseja chamar. Ponteiros e alças precisam ser convertidos para **LongPtr**. Por exemplo, a documentação para [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) fornece a assinatura a seguir: 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

Os parâmetros são definidos como:
  
|Parâmetro|Descrição|
|:-----|:-----|
|hKey [in]  <br/> |Uma  *alça*  para uma chave do Registro aberta.  <br/> |
|lpSubKey [in, optional]  <br/> |O nome da subchave de registro a ser aberta.  <br/> |
|ulOptions  <br/> |Esse parâmetro está reservado e deve ser zero.  <br/> |
|samDesired [in]  <br/> |Uma máscara que especifica os direitos de acesso desejado para a chave.  <br/> |
|phkResult [out]  <br/> |Um  *ponteiro*  para uma variável que recebe uma alça para a chave aberta.  <br/> |
   
No [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), a instrução **Declare** é definida como: 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>Posso converter ponteiros e alças em estruturas?
  
Sim. Confira o tipo **MSG** em Win32API_PtrSafe.txt: 
  
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

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a>Quando devo usar strptr varpt e objptr?
  
Você deve usar essas funções para recuperar ponteiros para cadeias de caracteres, variáveis e objetos, respectivamente. Na versão de 64 bits do Office, essas funções retornarão um **LongPtr** de 64 bits, que pode ser passado para instruções **Declare**. O uso dessas funções não mudou de versões anteriores do VBA. A única diferença é que elas agora retornam um **LongPtr**.
  
## <a name="see-also"></a>Confira também
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Anatomy of a Declare Statement](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

