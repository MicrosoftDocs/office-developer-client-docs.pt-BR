---
title: Criar XLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- dlls [excel 2007], chamando para excel, função xlAutoFree [Excel 2007], função xlAutoFree12 [Excel 2007], xlcall32.lib [Excel 2007], função xlAutoRegister [Excel 2007], xlcall.cpp [Excel 2007], função xlAutoRemove [ Excel 2007], função xlAddInManagerInfo [Excel 2007], função xlAutoAdd [Excel 2007], função xlAutoOpen [Excel 2007], função xlAutoClose [Excel 2007], DLLs [Excel 2007], transformando-se em XLLs, XLLs [Excel 2007], chamando para Excel, função xlAutoRegister12 [Excel 2007], xlcall.h [Excel 2007], função xlAddInManagerInfo12 [Excel 2007]
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 886b8e74f00f2e724785d43475ee0ffa3c922710
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706741"
---
# <a name="creating-xlls"></a>Criar XLLs

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se sua DLL é autônoma ou depende apenas de outras bibliotecas, você deve saber como habilitar o Microsoft Excel para acessar suas funções e comandos. Para saber mais, confira [Acessar DLLs no Excel](how-to-access-dlls-in-excel.md). 
  
No entanto, se sua DLL precisa acessar a funcionalidade do Excel (por exemplo, para obter o conteúdo de uma célula, chamar uma função de planilha ou interrogar o Excel para obter informações de espaço de trabalho), seu código deve ser capaz de retornar ao Excel.
  
A API do Excel C fornece várias funções que permitem que as DLLs retornem para o Excel. Para acessá-las, a DLL deve estar vinculada estaticamente em tempo de compilação com a biblioteca de 32 bits do Excel, xlcall32.lib. A biblioteca estática pode ser baixada da Microsoft como parte do Microsoft Excel 2013 XLL SDK, que inclui as versões de 32 e 64 bits desta biblioteca.
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Habilitando DLLs para retorno de chamada no Excel

Para que uma DLL possa acessar a funcionalidade no Excel e obter ou definir informações de espaço de trabalho, ela deve primeiro obter os endereços das funções de retorno de chamada do Excel **Excel4**, **Excel4v**, ** Excel12**, e **Excel12v**. Os dois últimos foram introduzidos no Excel 2007 e estão disponíveis em versões posteriores. Para acessar todos eles, o projeto DLL deve incluir referências aos seguintes arquivos do Excel 2013 XLL SDK. Se você deseja acessar apenas os dois primeiros retornos de chamada (em qualquer versão do Excel), seu projeto precisa incluir apenas os dois primeiros arquivos.
  
### <a name="xlcallh"></a>Xlcall. h

O arquivo xlcall. h contém os seguintes itens:
  
- Protótipos de função para todas as funções de retorno de chamada.
    
- Definições das estruturas de dados que os retornos de chamada usam para trocar dados entre as definições DLL / XLL e Excel e definições constantes de tipos de dados.
    
- Definições da função da API C e equivalentes de comando da planilha, funções de folha de macro e comandos do Excel com suporte.
    
- Definições dos valores de retorno da função de retorno de chamada.
    
Você deve usar a diretiva **#include** para esse arquivo, direta ou indiretamente por meio de outro arquivo de cabeçalho, em todos os arquivos que acessam a API C ou que manipulam os tipos de dados usados ​​pela API C. 
  
### <a name="xlcall32lib"></a>Xlcall32.lib

A biblioteca xlcall32 exporta os dois primeiros retornos de chamada **Excel4** e **Excel4v**e também a função**XlCallVer**. Sem uma referência a essa biblioteca em seu projeto, o vinculador não pode criar a XLL se você tiver usado qualquer um desses retornos de chamada em seu código. (Você pode obter os endereços dessas funções vinculando dinamicamente ao equivalente Xlcall32.dll que é copiado para o sistema como parte de uma instalação normal do Excel.) 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

As chamadas de retorno do Excel **Excel12** e **Excel12v** não serão exportadas na xlcall32. Isso garante que os projetos XLL que você cria a partir do Excel 2007 também funcionem com versões anteriores do Excel. O módulo Xlcall.cpp contém código para as funções **Excel12** e **Excel12v**, que chamam um ponto de entrada do Excel a partir do Excel 2007, ou retorna um valor de erro seguro se você estiver executando uma versão anterior do Excel. Você deve incluir este módulo em seu projeto se quiser criar uma XLL que seja executada a partir do Excel 2007 e que possa usar os novos tipos de dados que manipulam grades maiores e seqüências de caracteres Unicode mais longas. 
  
> [!NOTE]
> A partir do SDK do Excel 2010, esse arquivo pode ser compilado para XLLs de 32 e 64 bits. 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>Transformar DLLs em XLLs: Funções de Interface do Gerenciador de Suplementos

Um XLL é uma DLL que exporta vários procedimentos chamados pelo Excel ou pelo Gerenciador de suplemento do Excel. Estes procedimentos são descritos brevemente aqui e discutidos em detalhes no[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md). Todas essas retornos DLL de começam com o prefixo **xlAuto**. Apenas um deles, o comando **xlAutoOpen**, é necessário. Ele é chamado quando o suplemento é ativado e é normalmente usado para registrar funções e comandos XLL com o Excel e para executar outras tarefas de inicialização. As assinaturas de função e implementações de exemplo de todas as funções **xlAuto** são fornecidas nas seções posteriores. 
  
Embora **xlAutoOpen** seja a única função necessária desses retornos de chamada, seu suplemento também pode precisar exportar outros dependendo do seu comportamento. 
  
O Excel 2007 introduziu um novo tipo de dados, o **XLOPER12**, para acomodar grades maiores e para suportar longas cadeias de caracteres Unicode. **XLOPER12** está descrito adiante neste tópico. Enquanto as funções **xlAuto** obtêm ou retornam o tipo de dados antigo **XLOPER**, novas versões dessas funções que usam tipos de dados **XLOPER12** foram introduzidas no Excel 2007. Com exceção do **xlAutoFree12**, que você deve implementar às vezes, para evitar vazamentos de memória **XLOPER12**, você pode omitir com segurança toda as funções **xlAuto** da versão 12. Nesse caso, começando no Excel 2007, o Excel chama as versões **XLOPER**. 
  
### <a name="xlautoopen"></a>xlAutoOpen

O Excel chama a função [xlAutoOpen](xlautoopen.md) sempre que o XLL está ativado. O suplemento será ativado no início de uma sessão do Excel se estava ativo na última sessão do Excel que terminou normalmente. O suplemento é ativado se for carregado durante uma sessão do Excel. O suplemento pode ser desativado e reativado durante uma sessão do Excel e a função é chamada em reativação. 
  
Você deve usar **xlAutoOpen** para registrar XLL funções e comandos, inicializar estruturas de dados, personalizar a interface do usuário e assim por diante. 
  
Se o suplemento implementa e exporta a função [xlAutoRegister](xlautoregister-xlautoregister12.md) ou a função [xlAutoRegister12](xlautoregister-xlautoregister12.md) o Excel pode tentar ativar e registrar um comando ou função sem chamar a função **xlAutoOpen primeiro**. Nesse caso, você deve garantir que seu suplemento esteja suficientemente inicializado para que sua função ou comando funcione corretamente. Se não for, você deve falhar na tentativa de registrar a função ou o comando ou executar a inicialização necessária. 
  
### <a name="xlautoclose"></a>xlAutoClose

O Excel chama a função [xlAutoClose](xlautoclose.md) sempre que o XLL está desativado. O suplemento será desativado quando a sessão do Excel termina normalmente. Se o usuário desativar o suplemento durante uma sessão do Excel, a função é chamada. 
  
Você deve usar **xlAutoClose** para cancelar o registro de funções e comandos, liberar recursos, desfazer personalizações e assim por diante. 
  
> [!NOTE]
> Há um problema conhecido com o cancelamento de registro de funções e comandos. Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md). 
  
### <a name="xlautoadd"></a>xlAutoAdd

O Excel chama a [função xlAutoAdd](xlautoadd.md) sempre que o usuário ativa o XLL durante uma sessão do Excel usando o Gerenciador de Suplementos. Esta função não é chamada quando o Excel é iniciado e carrega um suplemento pré-instalado. 
  
Você pode usar essa função para exibir uma caixa de diálogo personalizada que informa ao usuário que o suplemento foi ativado, para ler ou gravar no registro ou para verificar as informações de licenciamento.
  
### <a name="xlautoremove"></a>xlAutoRemove

O Excel chama a função [xlAutoRemove](xlautoremove.md) sempre que o usuário desativa o XLL durante uma sessão do Excel usando o Gerenciador de Suplementos. Esta função não é chamada quando uma sessão do Excel é fechada, normalmente ou de forma anormal, com o suplemento instalado. 
  
Você pode usar essa função para exibir uma caixa de diálogo personalizada que informa ao usuário que o suplemento foi desativado ou para ler ou gravar no registro.

  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

O Excel chama a função [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) quando o Gerenciador de suplementos é chamado pela primeira vez em uma sessão do Excel. Se o Excel passar um argumento igual a 1, essa função deve retornar uma cadeia de caracteres (normalmente, o nome do suplemento); caso contrário, deve retornar **#VALUE!**.
  
A partir do Excel 2007, o Excel chama a função **xlAddInManagerInfo12** de preferência para a função **xlAddInManagerInfo** se ela for exportada pelo XLL. A função **xlAddInManagerInfo12** deve funcionar da mesma forma que a função **xlAddInManagerInfo** para evitar diferenças específicas de versão no comportamento do XLL. A função **xlAddInManagerInfo12** deve retornar um tipo de dados **XLOPER12**, enquanto a função **xlAddInManagerInfo** deve retornar um tipo de dados **XLOPER**. 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

O Excel chama a função [xlAutoRegister](xlautoregister-xlautoregister12.md) sempre que uma chamada foi feita para a função XLM **REGISTER**, ou a função [xlfRegister](xlfregister-form-1.md) equivalente da API C, com os tipos de retorno e argumento ausentes para a função que está sendo registrada. A função **xlAutoRegister** permite que o XLL pesquise suas listas internas de funções e comandos exportados para registrar a função com o argumento e retornar os tipos especificados. 
  
A partir do Excel 2007, o Excel chama a função **xlAddInRegister12** de preferência para a função **xlAddInRegister** se ela for exportada pelo XLL. 
  
> [!NOTE]
> Se **xlAddInRegister**/ **xlAddInRegister12** tentar registrar a função sem fornecer o argumento e tipos de retorno, ocorre um loop de chamada recursiva que, eventualmente, transborda a pilha de chamadas e faz com que o Excel feche ou pare de responder. 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

O Excel chama a função [xlAutoFree / xlAutoFree12](xlautofree-xlautofree12.md) logo após uma função de planilha XLL retornar um tipo de dados **XLOPER**/ ** XLOPER12** com um conjunto de sinalizadores que informa ao Excel que há memória que o XLL ainda precisa liberar. Isso permite que a XLL retorne matrizes, cadeias de caracteres e referências externas dinamicamente alocadas para a planilha sem vazamentos de memória. A partir do Excel 2007, o tipo de dados **XLOPER12** é suportado. Para saber mais, consulte [Gerenciamento de Memória no Excel](memory-management-in-excel.md).
  
> [!NOTE]
> A partir do Excel 2007, quando o Excel é configurado para usar o recálculo de planilha com vários threads, a função **xlAutoFree**/ **xlAutoFree12** é chamada no mesmo thread que foi usado para chamar a função que a retornou. A chamada para **xlAutoFree**/ **xlAutoFree12**
é sempre feita antes que as células subseqüentes da planilha sejam avaliadas nesse encadeamento. Isso simplifica o design seguro para thread em sua XLL. Para saber mais, confira [Recálculo com vários threads no Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>Criar XLLs de 64 bits

Excel e funções definidas pelo usuário podem ser executadas em sistemas operacionais de 64 bits para aproveitar os benefícios de desempenho em relação aos sistemas operacionais de 32 bits. O Excel passa valores nas estruturas **XLOPER12** com informações sobre os tipos de dados. Tenha cuidado ao converter valores entre a estrutura**XLOPER12** e tipos nativos como **int** ou ponteiros para preservar os valores de texto maior. 
  
## <a name="see-also"></a>Confira também



[Chamar funções de XLL no Assistente de Função ou nas caixas de diálogo Substituir](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)
  
[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

