---
title: Multithreading e contenção de memória no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading em excel, contenção de memória no Excel, funções [Excel 2007], thread-safe, thread-safe funciona memória local de segmento de [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb0eddfff2f34307143bb896fd451de357f2b639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765432"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading e contenção de memória no Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Versões anteriores do Microsoft Excel que o Excel 2007 usam um único segmento para todos os cálculos da planilha. No entanto, a partir do Excel 2007, Excel pode ser configurado para usar de 1 segmentos simultâneos de 1024 para cálculo da planilha. Em um computador com vários processadores ou vários núcleo, o número de threads padrão é igual ao número de processadores ou núcleos. Portanto, as células de thread-safe ou células que contêm apenas a funções que são thread-safe, podem ser reservadas para segmentos simultâneos, sujeito a lógica de recálculo usuais para serem calculadas após seus precedentes.
  
## <a name="thread-safe-functions"></a>Funções thread-Safe

A maioria das funções de planilha internas iniciada no Excel 2007 são thread-safe. Você também pode gravar e registrar as funções XLL como sendo thread-safe. O Excel usa um segmento (seu segmento principal) para chamar todos os comandos, funções thread-inseguras, funções **xlAuto** (exceto [xlAutoFree](xlautofree-xlautofree12.md) e **xlAutoFree12**) e COM e do Visual Basic para funções Applications (VBA).
  
Onde uma função XLL retorna uma **XLOPER** ou **XLOPER12** com **xlbitDLLFree** definido, o Excel usa o mesmo thread em que a chamada de função foi feita para chamar **xlAutoFree** ou **xlAutoFree12**. A chamada para **xlAutoFree** ou **xlAutoFree12** é feita antes da próxima chamada de função naquele segmento. 
  
Para os desenvolvedores XLL, existem benefícios para a criação de funções thread-safe:
  
- Eles permitem que o Excel para fazer o máximo de um computador com vários processadores ou vários núcleo.
    
- Eles abrem a possibilidade de usar servidores remotos muito mais eficiente do que pode ser realizado usando um único segmento.
    
Suponha que você tem um computador com processador único que tenha sido configurado para usar, digamos, *N* threads. Suponha que uma planilha está sendo executado se torne um grande número de chamadas para uma função XLL que por sua vez envia uma solicitação de dados ou de um cálculo a ser executada em um servidor remoto ou de um cluster de servidores. Sujeito a topologia da árvore de dependência, Excel poderia chamar os tempos de função N quase simultaneamente. Desde que o servidor ou servidores são suficientemente fast ou paralelo, o tempo de recálculo da planilha poderia ser reduzido em tanto quanto um fator de 1/s. 
  
A principal questão na escrita funções thread-safe está manipulando corretamente contenção de recursos. Isso geralmente significa contenção de memória, e ele pode ser dividido em dois problemas:
  
- Como criar memória que você sabe que será usado apenas por esse segmento.
    
- Como garantir que é acessada por vários threads memória compartilhada com segurança.
    
A primeira coisa para estar ciente é quais tipos de memória em um XLL pode ser acessado por todos os threads e o que seja acessível apenas pelo thread atualmente em execução.
  
 **Acessível por todos os threads**
  
- Variáveis, estruturas e instâncias da classe declarada fora o corpo de uma função.
    
- Variáveis estáticas declaradas dentro do corpo de uma função.
    
Nesses dois casos, a memória é definida reserve no bloco de memória da DLL criado para esta instância da DLL. Se outra instância do aplicativo carrega a DLL, ele obtém sua própria cópia de que a memória para que não haja nenhum contenção desses recursos de fora dessa instância da DLL.
  
 **Acessível somente pelo thread atual**
  
- Variáveis automáticas do código de função (incluindo argumentos da função).
    
Nesse caso, a memória é definida reserve na pilha para cada instância da chamada de função.
  
> [!NOTE]
> O escopo de memória alocada dinamicamente depende do escopo do ponteiro do que aponta para ela: se o ponteiro pode ser acessado por todos os threads, a memória também será. Se o ponteiro é uma variável automática em uma função, a memória alocada é efetivamente privada para esse segmento. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Memória acessível por apenas um segmento: memória Local de segmento

Visto que variáveis estáticas dentro do corpo de uma função são acessíveis por todos os threads, funções que usá-los não estão claramente thread-safe. Uma instância da função em um thread poderia ser a alteração do valor enquanto outra instância em outro thread é supondo que seja algo completamente diferente. 
  
Existem duas razões para declarar variáveis estáticas dentro de uma função:
  
1. Dados estáticos persistem de uma chamada para o próximo.
    
2. Um ponteiro para dados estáticos com segurança pode ser retornado pela função.
    
No caso do primeiro motivo, talvez você queira ter dados que persiste e tem significado para todas as chamadas para a função: talvez um contador simple que é incrementado toda vez que a função for chamada em qualquer segmento, ou uma estrutura que coleta dados de uso e desempenho nos noite Ry chamada. A pergunta é como proteger os dados compartilhados ou uma estrutura de dados. Isso é feito melhor usando a seção crítica conforme a próxima seção explica.
  
Se os dados são destinados apenas para uso por este thread, que pode ser o caso por motivo 1 e é sempre o caso por motivo 2, a pergunta é como criar memória persiste, mas só está acessível a partir do thread. Uma solução é usar o armazenamento de thread local (TLS) API.
  
Por exemplo, considere uma função que retorna um ponteiro para um **XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Essa função não é thread-safe porque um segmento pode retornar o estática **XLOPER12** enquanto outra é sobrescrevê-lo. A probabilidade disso acontecer é maior ainda se o **XLOPER12** precisa ser passado para **xlAutoFree12**. Uma solução é alocar **XLOPER12**, retornar um ponteiro para ele e implementar **xlAutoFree12** para que a memória **XLOPER12** propriamente dito é liberada. Essa abordagem é usada em muitas das funções de exemplo mostradas no [Gerenciamento de memória no Excel](memory-management-in-excel.md).
  
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

Essa abordagem é mais simples implementar que a abordagem descrita na próxima seção, que utiliza a API de TLS, mas ele tem algumas desvantagens. Em primeiro lugar, o Excel deve chamar **xlAutoFree**/ **xlAutoFree12** seja qual for o tipo de retornado **XLOPER**/ **XLOPER12**. Segundo, há um problema ao retornar **XLOPER**/ **XLOPER12**s são o valor de retorno de uma chamada a uma função de retorno de chamada da API C. **XLOPER**/ **XLOPER12** podem apontar para memória que precisa ser liberado pelo Excel, mas **XLOPER**/ **XLOPER12** propriamente dito deve ser liberado da mesma forma que ela foi alocada. Se tais **XLOPER**/ **XLOPER12** deve ser usado como o valor de retorno de uma função de planilha XLL, há um meio fácil para informar aos **xlAutoFree**/ **xlAutoFree12** da necessidade de livre ambos os ponteiros da maneira apropriada. (Definindo o **xlbitXLFree** e o **xlbitDLLFree** não resolve o problema, conforme o tratamento de **XLOPER/XLOPER12s** no Excel com ambos os conjunto é indefinido e pode ser alterado de versão para versão.) Para contornar esse problema, XLL pode fazer cópias profundas de todos os alocadas Excel **XLOPER/XLOPER12s** que ele retorna à planilha. 
  
Uma solução que evita essas limitações é preencher e retornar um segmento local **XLOPER/XLOPER12**, uma abordagem que necessita desse **xlAutoFree/xlAutoFree12** não libera o ponteiro **XLOPER/XLOPER12** em si. 
  
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

A próxima pergunta é como configurar e recuperar a memória de segmento locais, em outras palavras, como implementar a função **get_thread_local_xloper12** no exemplo anterior. Isso é feito usando o Thread TLS (armazenamento Local) API. A primeira etapa é obter um índice TLS usando o **TlsAlloc**, que basicamente deve ser lançada usando **TlsFree**. Ambas são melhor realizadas a partir da **DllMain**.
  
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

Depois de obter o índice, a próxima etapa é alocar um bloco de memória para cada segmento. A [Documentação de desenvolvimento do Windows](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx) recomenda fazer isso sempre que a função de retorno de chamada **DllMain** é chamada com um evento **DLL_THREAD_ATTACH** e liberar a memória em cada **DLL_THREAD_DETACH**. No entanto, seguir este conselhos causaria sua DLL fazer trabalho desnecessário para threads não é usado para o recálculo. 
  
Em vez disso, é melhor usar uma estratégia de alocação no primeiro uso. Primeiro, você precisará definir uma estrutura que você deseja alocar para cada segmento. Para os exemplos anteriores que retornam **XLOPERs** ou **XLOPER12s**, o seguinte é suficiente, mas você pode criar qualquer estrutura que atenda às suas necessidades.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

A função a seguir obtém um ponteiro para a instância do segmento local ou aloca um destes se esta for a primeira chamada.
  
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

Agora você pode ver como a memória do segmento local **XLOPER/XLOPER12** é obtida: primeiro, você obtém um ponteiro para a instância do segmento de **TLS_data**e, em seguida, você retorna um ponteiro para **XLOPER/XLOPER12** contidos nela, da seguinte maneira. 
  
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

As funções **mtr_safe_example_1** e **mtr_safe_example_2** podem ser registradas como funções de planilha de thread-safe quando você estiver executando o Excel. No entanto, você não pode misturar as duas abordagens em um XLL. Seu XLL só pode exportar uma implementação do **xlAutoFree** e **xlAutoFree12**e cada estratégia de memória exige uma abordagem diferente. Com **mtr_safe_example_1**, o ponteiro passado **xlAutoFree/xlAutoFree12** deve ser liberado junto com quaisquer dados para que ela aponta. Com **mtr_safe_example_2**, somente os dados apontado para devem ser liberados.
  
Windows também fornece uma função **GetCurrentThreadId**, que retorna a ID exclusivo em todo o sistema. do thread atual Isso oferece o desenvolvedor com outra maneira para tornar o thread de código seguros ou fazer seu thread de comportamento específico.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Memória acessível somente por mais de um segmento: seções críticas

Você deve proteger memória de leitura/gravação que possa ser acessada por mais de um segmento usando as seções críticas. Você precisa de uma seção crítica nomeada para cada bloco de memória que você queira proteger. Você pode inicializá-los durante a chamada para a função **xlAutoOpen** e liberá-los e defini-las como null durante a chamada para a função **xlAutoClose** . Em seguida, você precisa conter cada acesso ao bloco protegido dentro de um par de chamadas para **EnterCriticalSection** e **LeaveCriticalSection**. Apenas um segmento tem permissão para a seção crítica a qualquer momento. Aqui está um exemplo de como a inicialização, desinicialização e uso de uma seção chamada **g_csSharedTable**.
  
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

Talvez mais segura, de outra maneira de proteger um bloco de memória é criar uma classe que contém sua própria **CRITICAL_SECTION** e cujos construtor, destrutor e métodos accessor cuidam de seu uso. Essa abordagem tem a vantagem adicional de proteger os objetos que podem ser inicializados antes **xlAutoOpen** seja executado ou sobreviver depois **xlAutoClose** é chamado, mas você deve tomar cuidado sobre a criação de muitas seções críticas e o sistema operacional sobrecarga que isso seria criar. 
  
Quando você tem o código que precisa acessar mais de um bloco de memória protegida ao mesmo tempo, você precisa considerar com muito cuidado a ordem na qual as seções críticas entra e sai. Por exemplo, duas funções a seguir poderiam criar um bloqueio.
  
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

Se a primeira função de um segmento entra **g_csSharedTableA** enquanto o segundo em outro thread entra **g_csSharedTableB**, ambos os threads paralisar. A abordagem correta é entrar em uma ordem consistente e sair na ordem inversa, da seguinte maneira.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Onde for possível, é melhor do thread co-operation ponto de vista para isolar o acesso a blocos distintos, conforme mostrado aqui.
  
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

Onde há muita contenção para um recurso compartilhado, como solicitações de acesso de curta duração frequente, você deve considerar usando a capacidade da seção críticos para rotação. Essa é uma técnica que torna a espera pelo recurso menos intensivos de processador. Para fazer isso, você pode usar qualquer um dos **InitializeCriticalSectionAndSpinCount** ao inicializar a seção ou **SetCriticalSectionSpinCount** inicializado uma vez, para definir o número de vezes que o thread faz um loop antes de aguardar recursos se tornarem disponível. A operação de espera é cara, portanto a rotação evita isso se o recurso for liberado enquanto isso. Em um sistema de processador único, a contagem de rotações é efetivamente ignorada, mas você ainda pode especificá-lo sem causar nenhum dano. O Gerenciador de heap de memória utiliza uma contagem de rotação de 4000. Para obter mais informações sobre o uso das seções críticas, consulte a documentação do SDK do Windows. 
  
## <a name="see-also"></a>Confira também



[Gerenciamento de memória no Excel](memory-management-in-excel.md)
  
[Recálculo multithreaded no Excel](multithreaded-recalculation-in-excel.md)
  
[Gerenciador de suplemento e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

