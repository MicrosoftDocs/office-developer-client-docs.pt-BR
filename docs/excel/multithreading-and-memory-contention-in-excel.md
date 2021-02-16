---
title: Multithreading e contenção de memória no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading no excel, contenção de memória no Excel, funções [Excel 2007], thread-safe, funções thread-safe [Excel 2007], memória local de threads [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Aplicável a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301635"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading e contenção de memória no Excel

 **Aplicável a**: Excel 2013 | Office 2013 | Visual Studio 
  
Versões do Microsoft Excel anteriores ao Excel 2007 usam um único thread para todos os cálculos de planilha. No entanto, a partir do Excel 2007, o Excel pode ser configurado para usar de 1 a 1024 threads simultâneos para o cálculo de planilhas. Em um computador com vários processadores ou vários núcleos, o número padrão de threads é igual ao número de processadores ou núcleos. Portanto, células thread-safe, ou células que contenham apenas funções que são thread-safe, podem ser alocadas a threads simultâneos, sujeitas à lógica de recálculo comum que estabelece que elas precisam ser calculadas após seus precedentes.
  
## <a name="thread-safe-functions"></a>Funções thread-safe

A maioria das funções de planilha internas, a partir do Excel 2007, são thread-safe. Você também pode gravar e registrar funções XLL como sendo thread-safe. O Excel usa um thread (seu thread principal) para chamar todos os comandos, funções não thread-safe, funções **xlAuto** (exceto [xlAutoFree](xlautofree-xlautofree12.md) e **xlAutoFree12**) e funções COM e do Visual Basic for Applications (VBA).
  
Quando uma função XLL retorna **XLOPER** ou **XLOPER12** com o conjunto **xlbitDLLFree**, o Excel usa o mesmo de thread no qual a chamada de função foi feita para chamar **xlAutoFree** ou **xlAutoFree12**. A chamada para **xlAutoFree** ou **xlAutoFree12** é feita antes da próxima chamada de função nesse thread. 
  
Para desenvolvedores de XLL, há benefícios para a criação de funções thread-safe:
  
- Elas permitem que o Excel tire o máximo de proveito de um computador com vários processadores ou vários núcleos.
    
- Elas abrem a possibilidade de usar servidores remotos com muito mais eficiência do que pode ser feito usando um único thread.
    
Suponha que você tenha um computador com processador único que tenha sido configurado para usar *N* threads. Imagine uma planilha em execução que faz um grande número de chamadas para uma função XLL que, por sua vez, envia uma solicitação de dados ou de cálculo a um servidor remoto ou cluster de servidores. Dependendo da topologia da árvore de dependência, o Excel pode chamar a função N vezes quase simultaneamente. Desde que o servidor ou os servidores sejam suficientemente rápidos ou paralelos, o tempo de recálculo da planilha pode ser reduzido até um fator de 1/N. 
  
O principal problema na gravação de funções thread-safe é manipular a contenção de recursos corretamente. Isso geralmente significa contenção de memória e pode ser dividido em dois problemas:
  
- Como criar a memória que você sabe que só será usada por esse thread.
    
- Como garantir que a memória compartilhada seja acessada por vários threads com segurança.
    
A primeira coisa a ter em conta é qual memória em um XLL é acessível por todos os encadeamentos e qual é acessível apenas pelo encadeamento atualmente em execução.
  
 **Acessível por todos os threads**
  
- Variáveis, estruturas e instâncias de classes declaradas fora do corpo de uma função.
    
- Variáveis estáticas declaradas no corpo de uma função.
    
Nesses dois casos, a memória é reservada no bloco de memória da DLL criado para essa instância da DLL. Se outra instância de aplicativo carregar a DLL, ela obterá sua própria cópia dessa memória para que não haja contenção desses recursos de fora dessa instância da DLL.
  
 **Acessível apenas pelo thread atual**
  
- Variáveis automáticas no código de função (incluindo argumentos de função).
    
Nesse caso, a memória é reservada na pilha para cada instância da chamada de função.
  
> [!NOTE]
> O escopo da memória alocada dinamicamente depende do escopo do ponteiro que aponta para ela: se o ponteiro for acessível por todos os threads, o mesmo acontecerá com a memória. Se o ponteiro for uma variável automática em uma função, a memória alocada será efetivamente privada para esse segmento. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Memória acessível por apenas um thread: memória local de thread

Considerando que as variáveis estáticas dentro do corpo de uma função são acessíveis por todos os threads, as funções que as utilizam claramente não são thread-safe. Uma instância da função em um thread pode estar alterando o valor, enquanto outra instância em outro thread está assumindo que se trata de algo completamente diferente. 
  
Existem duas razões para declarar variáveis estáticas dentro de uma função:
  
1. Dados estáticos persistem de uma chamada para a seguinte.
    
2. Um ponteiro para dados estáticos pode ser retornado com segurança pela função.
    
No caso do primeiro motivo, talvez você queira ter dados que persistam e tenham significado para todas as chamadas à função: talvez um contador simples que seja incrementado toda vez que a função for chamada em qualquer thread ou uma estrutura que colete dados de uso e desempenho em todas as chamadas. A questão é como proteger os dados compartilhados ou a estrutura de dados. Isso é feito da melhor maneira usando a seção crítica, como a próxima seção explica.
  
Se os dados se destinam apenas ao uso por esse thread, o que pode ser o caso do motivo 1 e é sempre o caso do motivo 2, a questão é como criar uma memória que persista, mas que apenas seja acessível por esse thread. Uma solução é usar a API de armazenamento local de thread (TLS).
  
Por exemplo, considere uma função que retorne um ponteiro para um **XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Essa função não é thread-safe, pois um thread pode retornar o **XLOPER12** estático enquanto outro o sobrescreve. A probabilidade de isso acontecer será ainda maior se for necessário transmitir **XLOPER12** para **xlAutoFree12**. Uma solução é alocar um **XLOPER12**, retornar um ponteiro para ele e implementar **xlAutoFree12** para que a memória de **XLOPER12** propriamente dita seja liberada. Essa abordagem é usada em muitas das funções de exemplo mostradas em [Gerenciamento da memória no Excel](memory-management-in-excel.md).
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Essa abordagem é mais simples de implementar do que a abordagem descrita na próxima seção, que se baseia na API TLS, mas apresenta algumas desvantagens. Primeiro, o Excel deve chamar **xlAutoFree**/ **xlAutoFree12** seja qual for o tipo do **XLOPER**/ **XLOPER12** retornado. Em segundo lugar, há um problema ao retornar **XLOPER**/ **XLOPER12** s que são o valor de retorno de uma chamada para uma função de retorno de chamada da API C. O **XLOPER**/ **XLOPER12** pode apontar para uma memória que precisa ser liberada pelo Excel, mas o **XLOPER**/ **XLOPER12** propriamente dito deve ser liberado da mesma maneira com que foi alocado. Se esse **XLOPER**/ **XLOPER12** tiver que ser usado como o valor de retorno de uma função de planilha XLL, não existe uma maneira fácil de informar **xlAutoFree**/ **xlAutoFree12** sobre a necessidade de liberar ambos os ponteiros da maneira apropriada. (Definir **xlbitXLFree** e **xlbitDLLFree** não resolve o problema, pois o tratamento de **XLOPER/XLOPER12s** no Excel com ambos configurados é indefinido e pode mudar de versão para versão.) Para contornar esse problema, o XLL pode fazer cópias profundas de todos os **XLOPER/XLOPER12s** alocados pelo Excel que ele retorna à planilha. 
  
Uma solução que evita essas limitações é preencher e retornar um **XLOPER/XLOPER12** local de thread, uma abordagem que exige que **xlAutoFree/xlAutoFree12** não libere o próprio ponteiro **XLOPER/XLOPER12** propriamente dito. 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

A próxima pergunta é como configurar e recuperar a memória local de thread, em outras palavras, como implementar a função **get_thread_local_xloper12** no exemplo anterior. Isso é feito usando a API TLS (Armazenamento Local de Thread). A primeira etapa é obter um índice TLS usando **TlsAlloc**, que deve ser liberado usando **TlsFree**. Ambos são mais bem realizados a partir de **DllMain**.
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

Depois de obter o índice, a próxima etapa é alocar um bloco de memória para cada thread. A [Documentação de desenvolvimento do Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recomenda fazer isso toda vez que a função de retorno de chamada **DllMain** for chamada com um evento **DLL_THREAD_ATTACH** e liberando a memória em cada **DLL_THREAD_DETACH**. No entanto, seguir esse aviso faria com que a sua DLL fizesse um trabalho desnecessário para threads não usados para recálculo. 
  
Em vez disso, é melhor usar uma estratégia de alocação no primeiro uso. Primeiro, você precisa definir uma estrutura que queira alocar para cada thread. Para os exemplos anteriores que retornam **XLOPERs** ou **XLOPER12s**, o seguinte é suficiente, mas você pode criar qualquer estrutura que atenda às suas necessidades.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

A função a seguir obtém um ponteiro para a instância local de thread ou aloca um caso essa seja a primeira chamada.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Agora, você pode ver como a memória **XLOPER/XLOPER12** local de thread é obtida: primeiro, você obtém um ponteiro para a instância de **TLS_data** do thread e, em seguida, retorna um ponteiro para o **XLOPER/XLOPER12** contido nele, da seguinte maneira. 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

As funções **mtr_safe_example_1** e **mtr_safe_example_2** podem ser registradas como funções de planilha thread-safe quando você está executando o Excel. No entanto, não é possível combinar as duas abordagens em um único XLL. Seu XLL só pode exportar uma implementação de **xlAutoFree** e **xlAutoFree12**, e cada estratégia de memória requer uma abordagem diferente. Com **mtr_safe_example_1**, o ponteiro transmitido para **xlAutoFree/xlAutoFree12** deve ser liberado junto com quaisquer dados para os quais ele aponte. Com **mtr_safe_example_2**, somente os dados apontados devem ser liberados.
  
O Windows também fornece uma função **GetCurrentThreadId**, que retorna o ID exclusivo no âmbito do sistema do thread atual. Isso fornece ao desenvolvedor outra maneira de tornar o código thread-safe ou de tornar seu comportamento específico para o thread.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Memória acessível somente por mais de um thread: seções críticas

Você deve proteger a memória de leitura/gravação que pode ser acessada por mais de um thread usando seções críticas. É necessário ter uma seção crítica nomeada para cada bloco de memória que você deseja proteger. Essas seções podem ser inicializadas durante a chamada para a função **xlAutoOpen** e liberadas e definidas como nulas durante a chamada para a função **xlAutoClose**. Em seguida, você precisa conter cada acesso ao bloco protegido em um par de chamadas para **EnterCriticalSection** e **LeaveCriticalSection**. Apenas um thread é permitido na seção crítica a qualquer momento. Veja a seguir um exemplo de inicialização, cancelamento da inicialização e uso de uma seção chamada **g_csSharedTable**.
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Outra maneira, talvez mais segura, de proteger um bloco de memória é criar uma classe que contenha sua própria **CRITICAL_SECTION** e cujos métodos de construtor, destruidor e acessador cuidem do seu uso. Essa abordagem tem a vantagem adicional de proteger objetos que possam ser inicializados antes da execução de **xlAutoOpen** ou que possam sobreviver após a chamada de **xlAutoClose**. Porém, você deve ter cuidado ao criar muitas seções críticas e com a sobrecarga que isso criaria no sistema operacional. 
  
Quando existe um código que requer acesso a mais de um bloco de memória protegida ao mesmo tempo, é necessário considerar com muito cuidado a ordem de entrada e saída dessas seções críticas. Por exemplo, as duas funções a seguir podem criar um deadlock.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Se a primeira função em um thread inserir **g_csSharedTableA** enquanto a segunda em outro thread inserir **g_csSharedTableB**, ambos os segmentos travarão. A abordagem correta é entrar em uma ordem consistente e sair na ordem inversa, da seguinte maneira.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Sempre que possível, sob o ponto de vista da cooperação de threads, é melhor isolar o acesso a blocos distintos, conforme mostrado aqui.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Onde houver muita contenção por um recurso compartilhado, como solicitações frequentes de acesso de curta duração, considere usar a capacidade de rodízio da seção crítica. Essa é uma técnica que faz com que a espera pelo recurso exija o uso de menos recursos do processador. Para fazer isso, você pode usar **InitializeCriticalSectionAndSpinCount** ao inicializar a seção ou **SetCriticalSectionSpinCount** uma vez que esta for inicializada, para definir o número de vezes que o thread executa um loop antes de aguardar a disponibilização de recursos. A operação de espera é dispendiosa e, portanto, o rodízio evita isso quando o recurso é liberado nesse meio tempo. Em um sistema de processador único, a contagem de rodízio é efetivamente ignorada, mas você ainda pode especificá-la sem causar nenhum dano. O gerenciador de heap de memória usa uma contagem de rodízio de 4000. Para obter mais informações sobre o uso de seções críticas, consulte a documentação do Windows SDK. 
  
## <a name="see-also"></a>Confira também



[Gerenciamento de Memória no Excel](memory-management-in-excel.md)
  
[Recálculo com vários threads no Excel](multithreaded-recalculation-in-excel.md)
  
[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

