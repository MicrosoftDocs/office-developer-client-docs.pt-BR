---
title: Criando XLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- DLLs [excel 2007], ligações para excel, função xlAutoFree [Excel 2007], função xlAutoFree12 [Excel 2007],xlcall32.lib [Excel 2007], função xlAutoRegister [Excel 2007],xlcall.cpp [Excel 2007], xlAutoRemove função [Excel 2007], xlAddInManagerInfo função [Excel 2007], função xlAutoAdd [Excel 2007], função xlAutoOpen [Excel 2007], xlAutoClose função [Excel 2007], DLLs [Excel 2007], transformando em XLLs, XLLs [Excel 2007], ligações para Excel, função xlAutoRegister12 [Excel 2007],xlcall.h [Excel função de xlAddInManagerInfo12 de 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: 7754998f-4e13-4a37-9724-43b6ee6c919b
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: de347d34768c25adf0d96642b4fade781ae26a9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765273"
---
# <a name="creating-xlls"></a>Criando XLLs

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Se sua DLL é autônomo ou depende somente em outras bibliotecas, você deve saber como habilitar o Microsoft Excel acessar suas funções e comandos. Para obter mais informações, consulte [Acesso DLLs no Excel](how-to-access-dlls-in-excel.md). 
  
No entanto, se sua DLL precisar acessar a funcionalidade do Excel (por exemplo, para obter o conteúdo de uma célula, chamar uma função de planilha ou de investigar Excel para obter informações de espaço de trabalho), seu código deve ser capaz de retorno de chamada para o Excel.
  
A API C do Excel fornece várias funções que permitem DLLs para retorno de chamada para o Excel. Para acessar esses, a DLL deve ser vinculada estaticamente em tempo de compilação com a biblioteca do Excel de 32 bits, xlcall32. A biblioteca estática é página de download da Microsoft como parte do Microsoft Excel 2013 XLL SDK, que inclui as versões de 32 bits e 64 bits desta biblioteca.
  
## <a name="enabling-dlls-to-call-back-into-excel"></a>Habilitando DLLs a chamada para o Excel

Para uma DLL seja capaz de acessar a funcionalidade do Excel e obter ou definir informações de espaço de trabalho, ele deve primeiro obter os endereços das funções do retorno de chamada Excel **Excel4**, **Excel4v**, **Excel12**e **Excel12v**. As duas últimas introduzidas no Excel 2007 e estão disponíveis nas versões subsequentes. Para acessar todos esses, o projeto DLL deve incluir referências para os seguintes arquivos do Excel 2013 XLL SDK. Se você deseja acessar apenas os retornos de duas primeiras chamada (em qualquer versão do Excel), o seu projeto deve incluir somente os primeiros dois arquivos.
  
### <a name="xlcallh"></a>Xlcall. h

O arquivo de xlcall. h contém os seguintes itens:
  
- Protótipos de função para todas as funções de retorno de chamada.
    
- Definições das estruturas de dados que os retornos de chamada usam para trocar dados entre o Excel e DLL/XLL e tipos de dados constante.
    
- Definições de equivalentes de função e comando do C API do planilha, funções de folha de macro e comandos do Excel com suporte.
    
- Valores de retorno de definições de função de retorno de chamada.
    
Você deve usar o **#include** diretriz para esse arquivo, diretamente ou indiretamente por meio de outro arquivo de cabeçalho, em todos os arquivos que acessar a API C ou que lidam com tipos de dados que usa a API C. 
  
### <a name="xlcall32lib"></a>Xlcall32

A biblioteca xlcall32 exporta os dois primeiros retornos de chamada, **Excel4** e **Excel4v**e também a função **XlCallVer** . Sem uma referência a essa biblioteca em seu projeto, o vinculador não pode criar o XLL, se você tiver usado qualquer um desses retornos de chamada em seu código. (Você pode obter os endereços dessas funções vinculando dinamicamente a xlcall32 equivalentes que são copiados para seu sistema como parte de uma instalação normal do Excel). 
  
### <a name="xlcallcpp"></a>Xlcall.cpp

Os retornos de chamada do Excel **Excel12** e **Excel12v** não são exportados no xlcall32. Isso garante que os projetos XLL que você criar iniciada no Excel 2007 também funcionará com versões anteriores do Excel. O módulo Xlcall.cpp contém código para o **Excel12** e funções **Excel12v** , o qual ligar para uma entrada de Excel aponte iniciada no Excel 2007 ou retornam um valor de erro de segurança, se você estiver executando uma versão anterior do Excel. Você deve incluir esse módulo em seu projeto, se você quiser criar um XLL executado iniciando no Excel 2007 e o que é possível usar os novos tipos de dados que lidam com grades maiores e mais cadeias de caracteres Unicode. 
  
> [!NOTE]
> Iniciando com o SDK do Excel 2010, esse arquivo pode ser compilado para XLLs de 32 bits e 64 bits. 
  
## <a name="turning-dlls-into-xlls-add-in-manager-interface-functions"></a>Transformando DLLs em XLLs: Gerenciador de funções da Interface de suplemento

Um XLL é uma DLL que exporta vários procedimentos que são chamados pelo Excel ou o Gerenciador de suplemento do Excel. Estes procedimentos são descritos resumidamente aqui e abordados em detalhes no [Gerenciador de suplementos e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md). Todos esses retornos de chamada DLL começam com o prefixo **xlAuto**. Somente um destes procedimentos, o comando **xlAutoOpen**, é necessário. Ele é chamado quando o suplemento é ativado, e ele geralmente é utilizado para registrar as funções XLL e comandos com o Excel e outras tarefas de inicialização. As assinaturas de função e exemplos de implementações de todas as funções **xlAuto** são fornecidos nas seções posteriores. 
  
Embora **xlAutoOpen** seja a única pessoa necessária esses retornos de, seu suplemento talvez também precisa exportar outras pessoas dependendo do seu comportamento. 
  
Excel 2007 introduziu um novo tipo de dados, **XLOPER12**, para acomodar grades maiores e para oferecer suporte a cadeias de caracteres Unicode longas. **XLOPER12** é descrito mais adiante neste tópico. Enquanto funções **xlAuto** levar ou retornam o tipo de dados antigo **XLOPER**, novas versões dessas funções foram introduzidas no Excel 2007 que usam tipos de dados **XLOPER12** . Com exceção de **xlAutoFree12**, que em alguns casos, você deve implementar para evitar a memória **XLOPER12** vazamento, você com segurança pode omitir todas as versão 12 **xlAuto** funções, nesse caso, iniciando no Excel 2007, chamadas de Excel **XLOPER** versões. 
  
### <a name="xlautoopen"></a>xlAutoOpen

Excel chama a função [xlAutoOpen](xlautoopen.md) sempre que o XLL é ativado. O suplemento será ativado no início de uma sessão do Excel se ele estava ativo na última sessão Excel que terminou normalmente. O suplemento é ativado se ele for carregado durante uma sessão do Excel. O suplemento pode ser desativado reativado durante uma sessão do Excel e a função for chamada em reativação. 
  
Você deve usar **xlAutoOpen** para registrar os comandos e funções XLL, inicializar estruturas de dados, personalize a interface do usuário e assim por diante. 
  
Se seu suplemento implementa e exporta a função [xlAutoRegister](xlautoregister-xlautoregister12.md) ou a função [xlAutoRegister12](xlautoregister-xlautoregister12.md) , Excel poderá tentar ativar e registrar um comando ou uma função sem primeiro chamar a função **xlAutoOpen** . Nesse caso, você deve assegurar que o add-in é suficientemente inicializado para sua função ou o comando funcione corretamente. Se não for, você deve falhar ou a tentativa de registrar a função ou o comando ou realizar a inicialização necessária. 
  
### <a name="xlautoclose"></a>xlAutoClose

Excel chama a função [xlAutoClose](xlautoclose.md) sempre que o XLL é desativado. O suplemento será desativado quando uma sessão do Excel é encerrada normalmente. Se o usuário desativa o suplemento durante uma sessão do Excel, a função é chamada. 
  
Você deve usar **xlAutoClose** para cancelar o registro de funções e comandos, liberar recursos, desfazer personalizações e assim por diante. 
  
> [!NOTE]
> Há um problema conhecido com o cancelamento de registro de funções e comandos. Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md). 
  
### <a name="xlautoadd"></a>xlAutoAdd

Excel chama a [função xlAutoAdd](xlautoadd.md) sempre que o usuário ativa o XLL durante uma sessão do Excel usando o Gerenciador de suplemento. Essa função não é chamada quando o Excel é iniciado e carrega um suplemento pré-instalado. 
  
Você pode usar esta função para exibir uma caixa de diálogo personalizada que informa ao usuário que o suplemento foi ativado, para ler ou gravar no registro ou para verificar as informações de licenciamento.
  
### <a name="xlautoremove"></a>xlAutoRemove

Excel chama a função [xlAutoRemove](xlautoremove.md) sempre que o usuário desativa o XLL durante uma sessão do Excel usando o Gerenciador de suplemento. Essa função não é chamada quando uma sessão do Excel é fechado, normalmente ou modo anormal, com o suplemento instalado. 
  
Você pode usar esta função para exibir uma caixa de diálogo personalizada que informa ao usuário que o suplemento foi desativado, ou para ler ou gravar no registro.
  
### <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

Excel chama a função [xlAddInManagerInfo](xladdinmanagerinfo-xladdinmanagerinfo12.md) quando o Gerenciador de suplementos é invocado pela primeira vez em uma sessão do Excel. Se o Excel passa um argumento igual a 1, essa função deve retornar uma cadeia de caracteres (geralmente, o nome do add-in); Caso contrário, ele deverá retornar **#VALUE!**.
  
Iniciando no Excel 2007, Excel chama a função **xlAddInManagerInfo12** em preferência a função **xlAddInManagerInfo** se ele é exportado pelo XLL. A função **xlAddInManagerInfo12** deve funcionar da mesma maneira como a função **xlAddInManagerInfo** para evitar específicos da versão diferenças no comportamento da XLL. A função **xlAddInManagerInfo12** deve retornar um tipo de dados **XLOPER12** , enquanto a função **xlAddInManagerInfo** deve retornar um tipo de dados **XLOPER** . 
  
### <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

Excel chama a função [xlAutoRegister](xlautoregister-xlautoregister12.md) sempre que foi feita uma chamada para a função XLM **registrar**ou a função equivalente [xlfRegister](xlfregister-form-1.md) de API C, com o retorno e os tipos de argumento ausentes para a função que está sendo registrada. A função **xlAutoRegister** permite que o XLL pesquisar seus listas internas de funções exportadas e comandos para registrar a função com o argumento e retornar tipos especificados. 
  
Iniciando no Excel 2007, Excel chama a função **xlAddInRegister12** em preferência a função **xlAddInRegister** se ele é exportado pelo XLL. 
  
> [!NOTE]
> Se **xlAddInRegister**/ **xlAddInRegister12** tentam registrar a função sem fornecer o argumento e retornar tipos, uma recursiva chamar loop ocorre que eventualmente estourar a pilha de chamada e faz com que o Excel fechar ou parar respondendo. 
  
### <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

Excel chama a função [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md) logo depois que uma função de planilha XLL retorna **XLOPER**/ o tipo de dados**XLOPER12** com um sinalizador definido que informa que o Excel não há memória que o XLL precisa release. Isso permite que o XLL retornar alocadas dinamicamente matrizes, cadeias de caracteres e as referências externas à planilha sem vazamento de memória. Iniciando no Excel 2007, o tipo de dados **XLOPER12** é suportado. Para saber mais, consulte [Memory Management in Excel](memory-management-in-excel.md).
  
> [!NOTE]
> Iniciando no Excel 2007, quando Excel está configurado para usar o recálculo de planilha multithreaded, o **xlAutoFree**/ **xlAutoFree12** função é chamada no mesmo thread que foi usado apenas para chamar a função que retornados a ele. A chamada para **xlAutoFree**/ **xlAutoFree12** sempre é feita antes de alguma célula da planilha subsequentes é avaliada naquele segmento. Isso simplifica o design de thread-safe em seu XLL. Para obter mais informações, consulte [Multithreaded recálculo no Excel](multithreaded-recalculation-in-excel.md). 
  
### <a name="creating-64-bit-xlls"></a>Criando XLLs de 64 bits

Excel e funções definidas pelo usuário podem ser executados em sistemas operacionais de 64 bits para aproveitar os benefícios de desempenho sobre os sistemas operacionais de 32 bits. Excel passa valores nas estruturas **XLOPER12** que incluem informações sobre os tipos de dados. Tenha cuidado ao converter entre valores na estrutura **XLOPER12** e tipos nativos como **int** ou ponteiros para preservar os valores no tipo de maior. 
  
## <a name="see-also"></a>Confira também



[Funções do Assistente de função ou caixas de diálogo Replace XLL chamada](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
[Gerenciador de suplemento e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)
  
[Developing Excel XLLs](developing-excel-xlls.md)

