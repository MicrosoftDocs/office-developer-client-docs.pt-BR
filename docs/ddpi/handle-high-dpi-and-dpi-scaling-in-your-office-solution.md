---
title: Lidar com a sua solução do Office de escala DPI e DPI alto
description: Atualize sua solução do Office como painéis de tarefas personalizados ou controles ActiveX, para dar suporte a monitores DPI altos.
ms.date: 03/09/2019
localization_priority: Normal
ms.openlocfilehash: 0425e5e9dd0f060a6336888cfe6c236b39732080
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980464"
---
# <a name="handle-high-dpi-and-dpi-scaling-in-your-office-solution"></a><span data-ttu-id="e30fd-103">Lidar com a sua solução do Office de alta escala DPI e DPI</span><span class="sxs-lookup"><span data-stu-id="e30fd-103">Handle high DPI and DPI scaling in your Office solution</span></span>

<span data-ttu-id="e30fd-104">Várias configurações e exibição agora suportam altas resoluções DPI (pontos por polegada) e pode conectar a vários monitores com tamanhos diferentes e densidades pixel.</span><span class="sxs-lookup"><span data-stu-id="e30fd-104">Many computer and display configurations now support high DPI (dots-per-inch) resolutions, and can connect multiple monitors with different sizes and pixel densities.</span></span> <span data-ttu-id="e30fd-105">Isso exige aplicativos para ajustar quando o usuário move o aplicativo a um monitor com um DPI diferente ou altera o nível de zoom.</span><span class="sxs-lookup"><span data-stu-id="e30fd-105">This requires applications to adjust when the user moves the app to a monitor with a different DPI, or changes the zoom level.</span></span> <span data-ttu-id="e30fd-106">Aplicativos que não dão suporte para conjunto de escala DPI podem funcionar em monitores com baixo DPI, mas ficarão ampliadas e desfocadas quando exibida em um monitor com alto DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-106">Applications that don’t support DPI scaling might look fine on low DPI monitors, but will look stretched and blurry when shown on a high DPI monitor.</span></span> 

<span data-ttu-id="e30fd-107">Aplicativos do Office 2016, como o Word e Excel foram atualizados para responder às alterações em fator de escala.</span><span class="sxs-lookup"><span data-stu-id="e30fd-107">Office 2016 applications, such as Word and Excel, have been updated to respond to changes in scale factor.</span></span> <span data-ttu-id="e30fd-108">No entanto, sua solução do Office também deve responder às alterações para mostrar corretamente quando o DPI é alterado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-108">However, your Office solution must also respond to changes to draw correctly when the DPI changes.</span></span> <span data-ttu-id="e30fd-109">Este artigo descreve como o Office tem suporte para DPI dinâmico e as medidas que você pode tomar para garantir a melhor experiência de sua solução de extensibilidade do identificador Office DPI de dimensionamento de visualização.</span><span class="sxs-lookup"><span data-stu-id="e30fd-109">This article describes how Office supports dynamic DPI, and what steps you can take to ensure the best viewing experience for your Office extensibility solution to handle DPI scaling.</span></span> 

## <a name="dpi-scaling-symptoms-in-your-solution"></a><span data-ttu-id="e30fd-110">Sintomas de dimensionamento DPI em sua solução</span><span class="sxs-lookup"><span data-stu-id="e30fd-110">DPI scaling symptoms in your solution</span></span>

<span data-ttu-id="e30fd-111">Windows aplica DPI para dimensionar quando um aplicativo é movido de uma exibição para outra exibição com um DPI diferente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-111">Windows applies DPI scaling when an application is moved from one display to another display with a different DPI.</span></span> <span data-ttu-id="e30fd-112">Isso ocorre em cenários como arrastar um aplicativo para outro monitor diferente ou encaixar seu laptop.</span><span class="sxs-lookup"><span data-stu-id="e30fd-112">This happens in scenarios such as dragging an application to a different monitor or docking your laptop.</span></span> <span data-ttu-id="e30fd-113">Se a sua solução do Office é afetada negativamente por escala DPI, você verá uma ou mais dos seguintes sintomas:</span><span class="sxs-lookup"><span data-stu-id="e30fd-113">If your Office solution is adversely affected by DPI scaling, you will see one or more of the following symptoms:</span></span>

- <span data-ttu-id="e30fd-114">As janelas mostram no local errado ou tiver dimensionamento incorreto.</span><span class="sxs-lookup"><span data-stu-id="e30fd-114">The windows draw in the wrong location or have incorrect sizing.</span></span>
- <span data-ttu-id="e30fd-115">Elementos como rótulos e botões são exibidos no lugar errado na janela da solução.</span><span class="sxs-lookup"><span data-stu-id="e30fd-115">Elements such as buttons and labels appear in the wrong location in your solution’s window.</span></span>
- <span data-ttu-id="e30fd-116">Fontes e imagens aparecem muito pequenos, muito grandes ou no local errado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-116">Fonts and images appear too small, too large or in the wrong location.</span></span>

<span data-ttu-id="e30fd-117">Os seguintes tipos de soluções do Office podem ser afetados por conjunto de escala DPI:</span><span class="sxs-lookup"><span data-stu-id="e30fd-117">The following types of Office solutions can be affected by DPI scaling:</span></span>

- <span data-ttu-id="e30fd-118">Suplementos VSTO</span><span class="sxs-lookup"><span data-stu-id="e30fd-118">VSTO Add-ins</span></span>
- <span data-ttu-id="e30fd-119">Painéis de Tarefas Personalizados</span><span class="sxs-lookup"><span data-stu-id="e30fd-119">Custom task panes</span></span>
- <span data-ttu-id="e30fd-120">Suplementos COM</span><span class="sxs-lookup"><span data-stu-id="e30fd-120">COM Add-ins</span></span>
- <span data-ttu-id="e30fd-121">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="e30fd-121">ActiveX controls</span></span>
- <span data-ttu-id="e30fd-122">Extensões de faixa de opções</span><span class="sxs-lookup"><span data-stu-id="e30fd-122">Ribbon extensions</span></span>
- <span data-ttu-id="e30fd-123">Servidores OLE</span><span class="sxs-lookup"><span data-stu-id="e30fd-123">Ole servers</span></span>
- <span data-ttu-id="e30fd-124">Suplementos do Office web</span><span class="sxs-lookup"><span data-stu-id="e30fd-124">Office web add-ins</span></span>

## <a name="windows-dpi-awareness-modes"></a><span data-ttu-id="e30fd-125">Modos de percepção DPI do Windows</span><span class="sxs-lookup"><span data-stu-id="e30fd-125">Windows DPI awareness modes</span></span>

<span data-ttu-id="e30fd-126">Neste artigo vamos nos referir aos modos de percepção DPI é compatível com Windows.</span><span class="sxs-lookup"><span data-stu-id="e30fd-126">Throughout this article we’ll refer to the DPI awareness modes that Windows supports.</span></span> <span data-ttu-id="e30fd-127">Cada modo de percepção DPI é compatível com diferentes recursos, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e30fd-127">Each DPI awareness mode supports different capabilities, as described in the following table.</span></span> <span data-ttu-id="e30fd-128">Esta é uma descrição simplificada de modos para explicar como soluções do Office compatíveis.</span><span class="sxs-lookup"><span data-stu-id="e30fd-128">This is a simplified description of the modes to explain how Office solutions support them.</span></span> <span data-ttu-id="e30fd-129">Confira mais informações sobre os modos de percepção DPI [desenvolvimento de aplicativos de área de trabalho do alto DPI no Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span><span class="sxs-lookup"><span data-stu-id="e30fd-129">For more information about the DPI awareness modes, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span></span>

|<span data-ttu-id="e30fd-130">Modo</span><span class="sxs-lookup"><span data-stu-id="e30fd-130">Mode</span></span>  |<span data-ttu-id="e30fd-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="e30fd-131">Description</span></span>  |<span data-ttu-id="e30fd-132">Quando alterações DPI</span><span class="sxs-lookup"><span data-stu-id="e30fd-132">When DPI changes</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="e30fd-133">DPI desconhecido</span><span class="sxs-lookup"><span data-stu-id="e30fd-133">DPI unaware</span></span> |  <span data-ttu-id="e30fd-134">Aplicativo sempre renderizado como se estivesse em uma exibição com valor de 96 DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-134">Application always renders as if it is on a display with a DPI value of 96.</span></span> |  <span data-ttu-id="e30fd-135">Aplicativo é bitmap alongado para o tamanho esperado em exibir primário e secundário.</span><span class="sxs-lookup"><span data-stu-id="e30fd-135">Application is bitmap stretched to expected size on primary and secondary displays.</span></span>    |
|<span data-ttu-id="e30fd-136">DPI ciente do sistema</span><span class="sxs-lookup"><span data-stu-id="e30fd-136">System DPI aware</span></span> |  <span data-ttu-id="e30fd-137">Aplicativo detecta DPI do monitor principal conectado ao fazer logon do Windows, mas não pode responder as alterações DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-137">Application detects the DPI of the primary connected monitor at Windows login but cannot respond to DPI changes.</span></span> <span data-ttu-id="e30fd-138">Para obter mais informações, consulte a seção [Configurar o Windows para corrigir aplicativos borrados](#configure-windows-to-fix-blurry-apps) neste artigo.</span><span class="sxs-lookup"><span data-stu-id="e30fd-138">For more information, see the [Configure Windows to fix blurry apps](#configure-windows-to-fix-blurry-apps) section in this article.</span></span>  | <span data-ttu-id="e30fd-139">O Aplicativo é bitmap alongado quando movidas para uma nova exibição com um DPI diferente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-139">Application is bitmap stretched when moved to a new display with a different DPI.</span></span>    |
|<span data-ttu-id="e30fd-140">Por Monitor DPI ciente</span><span class="sxs-lookup"><span data-stu-id="e30fd-140">Per Monitor DPI aware</span></span> |  <span data-ttu-id="e30fd-141">O Aplicativo é capaz de redesenho próprio corretamente quando o DPI é alterado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-141">Application is capable of redrawing itself correctly when the DPI changes.</span></span>  |   <span data-ttu-id="e30fd-142">O Windows enviará notificações DPI para janelas de nível superior do aplicativo para que possa reemitir quando o DPI for alterado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-142">Windows will send DPI notifications to top-level windows in the application so that it can redraw when the DPI changes.</span></span>     |
|<span data-ttu-id="e30fd-143">Por Monitor v2</span><span class="sxs-lookup"><span data-stu-id="e30fd-143">Per Monitor v2</span></span> |  <span data-ttu-id="e30fd-144">O Aplicativo é capaz de redesenho próprio corretamente quando o DPI é alterado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-144">Application is capable of redrawing itself correctly when the DPI changes.</span></span>  |   <span data-ttu-id="e30fd-145">O Windows enviará notificações DPI ao nível superior e janelas de criança para que o aplicativo possa reemitir quando o DPI for alterado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-145">Windows will send DPI notifications to both top-level and child windows so that the application can redraw when the DPI changes.</span></span> |

## <a name="how-office-supports-dpi-scaling"></a><span data-ttu-id="e30fd-146">Como o Office dá suporte de escala DPI</span><span class="sxs-lookup"><span data-stu-id="e30fd-146">How Office supports DPI scaling</span></span>

<span data-ttu-id="e30fd-147">O fator mais importante em determinar como sua solução do Office pode lidar com conjunto de escala DPI é se a solução for uma janela de nível superior ou em uma janela de criança.</span><span class="sxs-lookup"><span data-stu-id="e30fd-147">The most significant factor in determining how your Office solution can handle DPI scaling is whether your solution is a top-level window, or a child window.</span></span> <span data-ttu-id="e30fd-148">A imagem seguinte mostra alguns exemplos de soluções do Office executando como nível superior ou janelas de criança, e o modo de percepção DPI, eles usarão no Windows (1803) de atualização de abril de 2018 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="e30fd-148">The following picture shows a few examples of Office solutions running as top-level or child windows, and which DPI awareness mode they will use on Windows April 2018 Update (1803) and later.</span></span>

![Excel hospedagem um controle ActiveX e painel de tarefas personalizado, como janelas de criança.](./media/office-dpi-awareness-for-solution-types.png)

<span data-ttu-id="e30fd-152">Nesta imagem:</span><span class="sxs-lookup"><span data-stu-id="e30fd-152">In this image:</span></span>
- <span data-ttu-id="e30fd-153">A janela de nível superior VSTO/COM está por Monitor DPI ciente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-153">The COM/VSTO top-level window is Per Monitor DPI aware.</span></span>
- <span data-ttu-id="e30fd-154">A janela de criança de controle ActiveX é DPI de sistema ciente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-154">The ActiveX control child window is System DPI aware.</span></span>
- <span data-ttu-id="e30fd-155">A janela de nível superior do Office está por Monitor DPI ciente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-155">The Office top-level window is Per Monitor DPI aware.</span></span>
- <span data-ttu-id="e30fd-156">A janela de criança do painel de tarefas personalizado é DPI do sistema ciente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-156">The custom task pane child window is System DPI aware.</span></span>

## <a name="managing-thread-dpi-context"></a><span data-ttu-id="e30fd-157">Gerenciar o contexto DPI da conversa</span><span class="sxs-lookup"><span data-stu-id="e30fd-157">Managing thread DPI context</span></span>

<span data-ttu-id="e30fd-158">Quando inicia o aplicativo do Office host, sua conversa principal é executada no contexto ciente Per DPI Monitor.</span><span class="sxs-lookup"><span data-stu-id="e30fd-158">When the host Office app starts, its main thread runs in Per Monitor DPI aware context.</span></span> <span data-ttu-id="e30fd-159">Quando o código de solução cria conversas ou recebe chamadas do Office, você precisa gerenciar contexto DPI conversa.</span><span class="sxs-lookup"><span data-stu-id="e30fd-159">When your solution code creates threads, or receives calls from Office, you need to manage the thread DPI context.</span></span>

### <a name="creating-new-threads-with-the-correct-dpi-context"></a><span data-ttu-id="e30fd-160">Criar novas conversas com o contexto DPI correto</span><span class="sxs-lookup"><span data-stu-id="e30fd-160">Creating new threads with the correct DPI context</span></span>

<span data-ttu-id="e30fd-161">Se a sua solução cria conversas adicionais, o Office forçará as conversas no contexto ciente Per DPI Monitor.</span><span class="sxs-lookup"><span data-stu-id="e30fd-161">If your solution creates additional threads, Office will force the threads into Per Monitor DPI aware context.</span></span> <span data-ttu-id="e30fd-162">Se o código espera um contexto diferente, você precisa usar a função [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) para definir a percepção de conversa esperada DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-162">If your code expects a different context, you need to use the [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) function to set the expected thread DPI awareness.</span></span> 

### <a name="build-a-context-block-for-incoming-thread-calls"></a><span data-ttu-id="e30fd-163">Criar um bloco de contexto conversa para chamadas de entrada</span><span class="sxs-lookup"><span data-stu-id="e30fd-163">Build a context block for incoming thread calls</span></span>

![Diagrama que mostra o bloco de contexto no aplicativo do Office migrando conversa para o contexto de sistema ciente chamados para janela de nível superior.](./media/thread-dpi-awareness-context-block.png)

<span data-ttu-id="e30fd-165">Sua solução interagirá com seu aplicativo do Office host, assim você terá chamadas de entrada para sua solução do Office como retornos de evento.</span><span class="sxs-lookup"><span data-stu-id="e30fd-165">Your solution will interact with its host Office app, so you will have incoming calls to your solution from Office such as event callbacks.</span></span> <span data-ttu-id="e30fd-166">Quando o Office chamada sua solução, tem um bloco de contexto que força o contexto de conversa a ser sistema no contexto ciente DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-166">When Office calls your solution, it has a context block that forces the thread context to be in System DPI Aware context.</span></span> <span data-ttu-id="e30fd-167">Você deve alterar o contexto de conversa para corresponder a percepção DPI da janela.</span><span class="sxs-lookup"><span data-stu-id="e30fd-167">You must change the thread context to match the DPI awareness of your window.</span></span> <span data-ttu-id="e30fd-168">Você pode implementar um bloco de contexto semelhante para alternar o contexto de conversa para chamadas de entrada.</span><span class="sxs-lookup"><span data-stu-id="e30fd-168">You can implement a similar context block to switch the thread context on incoming calls.</span></span> <span data-ttu-id="e30fd-169">Use a função [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) para alterar o contexto de acordo com o contexto da janela.</span><span class="sxs-lookup"><span data-stu-id="e30fd-169">Use the [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) function to change the context to match your window context.</span></span> 

> [!NOTE]
> <span data-ttu-id="e30fd-170">O bloco do contexto deverá restaurar o contexto de conversa DPI original antes de chamar outros componentes fora do seu código solução.</span><span class="sxs-lookup"><span data-stu-id="e30fd-170">Your context block should restore the original DPI thread context before calling other components outside of your solution code.</span></span>

#### <a name="managed-code-context-block"></a><span data-ttu-id="e30fd-171">Gerenciamento de bloco de contexto de código</span><span class="sxs-lookup"><span data-stu-id="e30fd-171">Managed code context block</span></span>

<span data-ttu-id="e30fd-172">O código de exemplo a seguir mostra como criar seu próprio bloco de contexto.</span><span class="sxs-lookup"><span data-stu-id="e30fd-172">The following example code shows how to construct your own context block.</span></span>

```csharp
public struct DPI_AWARENESS_CONTEXT
        {
            private IntPtr value;

            private DPI_AWARENESS_CONTEXT(IntPtr value)
            {
                this.value = value;
            }

            public static implicit operator DPI_AWARENESS_CONTEXT(IntPtr value)
            {
                return new DPI_AWARENESS_CONTEXT(value);
            }

            public static implicit operator IntPtr(DPI_AWARENESS_CONTEXT context)
            {
                return context.value;
            }

            public static bool operator ==(IntPtr context1, DPI_AWARENESS_CONTEXT context2)
            {
                return AreDpiAwarenessContextsEqual(context1, context2);
            }

            public static bool operator !=(IntPtr context1, DPI_AWARENESS_CONTEXT context2)
            {
                return !AreDpiAwarenessContextsEqual(context1, context2);
            }

            public override bool Equals(object obj)
            {
                return base.Equals(obj);
            }

            public override int GetHashCode()
            {
                return base.GetHashCode();
            }
        }

        private static DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_HANDLE = IntPtr.Zero;

        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_INVALID = IntPtr.Zero;
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_UNAWARE = new IntPtr(-1);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_SYSTEM_AWARE = new IntPtr(-2);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE = new IntPtr(-3);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 = new IntPtr(-4);

        public static DPI_AWARENESS_CONTEXT[] DpiAwarenessContexts =
        {
            DPI_AWARENESS_CONTEXT_UNAWARE,
            DPI_AWARENESS_CONTEXT_SYSTEM_AWARE,
            DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE,
            DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2
        };

class DPIContextBlock : IDisposable
    {
        private DPI_AWARENESS_CONTEXT resetContext;
        private bool disposed = false;

        public DPIContextBlock(DPI_AWARENESS_CONTEXT contextSwitchTo)
        {
            resetContext = SetThreadDpiAwarenessContext(contextSwitchTo);
         }

        public void Dispose()
        {
            Dispose(true);
            GC.SuppressFinalize(this);
        }

        protected virtual void Dispose(bool disposing)
        {
            if (!disposed)
            {
                if (disposing)
                {
                    SetThreadDpiAwarenessContext(resetContext);
                }
            }
            disposed = true;
        }
    }
```

#### <a name="native-code-context-block"></a><span data-ttu-id="e30fd-173">Bloco do contexto de código nativo</span><span class="sxs-lookup"><span data-stu-id="e30fd-173">Native code context block</span></span>

```cpp
#include <winuser.h>
/* DpiAwarenessContextBlock can be used to simplify setting and resetting the DPI_AWARENESS_CONTEXT of
the current thread.  When the object is constructed, the DPI_AWARENESS_CONTEXT is set, and when the object is
destructed, the DPI awareness context is reverted to the previous awareness context at construct time.

This object allows us to write code such as:

// Thread state is currently DPI_AWARENESS_SYSTEM_AWARE
if (condition)
{
DpiAwarenessContextBlock perMonitorAware(DPI_AWARENESS_PER_MONITOR_AWARE);
... // Create a top-level hwnd with the current thread state, DPI_AWARENESS_PER_MONITOR_AWARE
}
// Thread state automatically returns to DPI_AWARENESS_SYSTEM_AWARE

*/
class DpiAwarenessContextBlock
{
public:
      DpiAwarenessContextBlock(DPI_AWARENESS_CONTEXT dpiContext) noexcept;
      ~DpiAwarenessContextBlock();

      // Copy and move are not to be used with these context objects
      DpiAwarenessContextBlock(const DpiAwarenessContextBlock&) = delete;
      DpiAwarenessContextBlock(DpiAwarenessContextBlock&&) = delete;

private:
      DPI_AWARENESS_CONTEXT m_contextReversalType;
      bool m_doContextSwitch;
};

inline DpiAwarenessContextBlock::DpiAwarenessContextBlock(DPI_AWARENESS_CONTEXT dpiContext) noexcept
{
      m_contextReversalType = SetThreadDpiAwarenessContext(dpiContext);
}

inline DpiAwarenessContextBlock::~DpiAwarenessContextBlock()
{
      SetThreadDpiAwarenessContext(m_contextReversalType);
}
```

<h2 id="top-level-window-management"><span data-ttu-id="e30fd-174">Gerenciamento de nível superior de janelas</span><span class="sxs-lookup"><span data-stu-id="e30fd-174">Top-level window management</span></span></h2>

<span data-ttu-id="e30fd-175">Ao iniciarem aplicativos do Office, uma chamada é feita para [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) como DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE.</span><span class="sxs-lookup"><span data-stu-id="e30fd-175">When Office applications start, a call is made to [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) as DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE.</span></span> <span data-ttu-id="e30fd-176">Nesse contexto as alterações DPI serão enviadas ao HWND todas as janelas de nível superior no processo que estejam em execução de acordo com o Monitor DPI ciente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-176">In this context, DPI changes are sent to the HWND of any top-level windows in the process that are running as Per Monitor DPI aware.</span></span> <span data-ttu-id="e30fd-177">Janelas de nível superior são janelas do aplicativo do Office e as janelas de nível superior adicionais criadas pela sua solução.</span><span class="sxs-lookup"><span data-stu-id="e30fd-177">Top-level windows are the Office application window, and any additional top-level windows created by your solution.</span></span> <span data-ttu-id="e30fd-178">Quando um aplicativo do Office é movido para uma nova exibição, será notificado para que ele dinamicamente dimensione e desenhe corretamente o DPI da tela de nova.</span><span class="sxs-lookup"><span data-stu-id="e30fd-178">When an Office application is moved to a new display, it gets notified so that it can dynamically scale and draw correctly in the DPI of the new display.</span></span> <span data-ttu-id="e30fd-179">Sua solução do Office pode criar janelas de nível superior que estão em qualquer modo de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-179">Your Office solution can create top-level windows that are in any DPI awareness mode.</span></span> <span data-ttu-id="e30fd-180">As janelas de nível superior podem também responder às alterações DPI ouvir a mensagem do Windows para as alterações.</span><span class="sxs-lookup"><span data-stu-id="e30fd-180">Your top-level windows can also respond to DPI changes by listening to Windows messages for the changes.</span></span>

<span data-ttu-id="e30fd-181">Se você criar janelas de criança que são como pais para a janela de nível superior, você pode configurá-los de qualquer modo de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-181">If you create child windows that are parented to your top-level window, you can also set them to any DPI awareness mode.</span></span> <span data-ttu-id="e30fd-182">No entanto, se você usar o modo ciente por DPI Monitor, as janelas de criança não receberão notificações de alteração DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-182">However, if you use Per Monitor DPI aware mode, your child windows will not receive DPI change notifications.</span></span>  <span data-ttu-id="e30fd-183">Confira mais informações sobre modos de percepção Windows DPI [desenvolvimento de aplicativos de área de trabalho DPI alto no Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span><span class="sxs-lookup"><span data-stu-id="e30fd-183">For more information about Windows DPI awareness modes, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span></span>

## <a name="child-window-management"></a><span data-ttu-id="e30fd-184">Gerenciamento de janelas</span><span class="sxs-lookup"><span data-stu-id="e30fd-184">Child window management</span></span>

<span data-ttu-id="e30fd-185">Ao trabalhar com controles ActiveX e painéis de tarefas personalizados, o Office cria a solução janelas de criança.</span><span class="sxs-lookup"><span data-stu-id="e30fd-185">When working with ActiveX controls and custom task panes, Office creates the child window for your solution.</span></span> <span data-ttu-id="e30fd-186">Criar janelas adicionais janelas de criança, mas você precisa considerar janela pais DPI ciente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-186">You can create additional child windows, but you have to be aware of the parent window DPI awareness.</span></span> <span data-ttu-id="e30fd-187">Office será executado no modo de percepção Per DPI Monitor, que significa que qualquer janelas de criança em sua solução não receberá notificações de alteração DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-187">Office runs in Per Monitor DPI awareness mode, which means any child windows in your solution will not get DPI change notifications.</span></span> <span data-ttu-id="e30fd-188">Apenas per modo Monitor v2 oferece suporte ao envio DPI para altera para janelas de criança (o Office não tem suporte por Monitor v2).</span><span class="sxs-lookup"><span data-stu-id="e30fd-188">Only Per Monitor v2 mode supports sending DPI changes to child windows (Office does not support Per Monitor v2).</span></span> <span data-ttu-id="e30fd-189">No entanto, para controles ActiveX, há uma solução alternativa.</span><span class="sxs-lookup"><span data-stu-id="e30fd-189">However, for ActiveX controls, there is a workaround.</span></span> <span data-ttu-id="e30fd-190">Para saber mais, confira a [controles ActiveX](#activex-controls) seção neste artigo.</span><span class="sxs-lookup"><span data-stu-id="e30fd-190">For more information, see the [ActiveX controls](#activex-controls) section later in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="e30fd-191">Se sua janela de criança cria uma janela de nível superior, você pode usar qualquer modo de percepção DPI da nova janela de nível superior.</span><span class="sxs-lookup"><span data-stu-id="e30fd-191">If your child window creates a top-level window, you can use any DPI awareness mode for the new top-level window.</span></span> <span data-ttu-id="e30fd-192">Para saber mais sobre o gerenciamento de janelas de nível superior, confira a seção deste artigo [gerenciamento de janelas de nível superior](#top-level-window-management).</span><span class="sxs-lookup"><span data-stu-id="e30fd-192">For more information about managing top-level windows, see the [Top-level window management](#top-level-window-management) section in this article.</span></span>

<span data-ttu-id="e30fd-193">Você verá dois modos DPI diferentes aplicados a janela de criança, dependendo de qual versão do Windows 10 Office está em execução.</span><span class="sxs-lookup"><span data-stu-id="e30fd-193">You will see two different DPI modes applied to your child window, depending on which version of Windows 10 Office is running on.</span></span>

### <a name="office-dpi-behavior-on-windows-fall-creators-update-1709"></a><span data-ttu-id="e30fd-194">Comportamento DPI do Office no Windows Fall Creators Update (1709)</span><span class="sxs-lookup"><span data-stu-id="e30fd-194">Office DPI behavior on Windows Fall Creators Update (1709)</span></span>

<span data-ttu-id="e30fd-195">Como os aplicativos do Office usam o modo de percepção por Monitor, janelas filho da solução também serão criadas no modo de percepção Per DPI Monitor.</span><span class="sxs-lookup"><span data-stu-id="e30fd-195">Because Office apps use Per Monitor awareness mode, your solution’s child windows will also be created in Per Monitor DPI awareness mode.</span></span> <span data-ttu-id="e30fd-196">Isso significa que o Windows espera que a sua solução de atualização quando um novo DPI de desenho.</span><span class="sxs-lookup"><span data-stu-id="e30fd-196">This means Windows expects your solution to update when drawing in a new DPI.</span></span>  <span data-ttu-id="e30fd-197">Como a janela não é possível receber notificações de alteração DPI, interface do usuário da solução pode estar incorreto.</span><span class="sxs-lookup"><span data-stu-id="e30fd-197">Because your window cannot get DPI change notifications, your solution’s UI might be incorrect.</span></span> 

![Diagrama mostrando janelas filho em execução no contexto ciente Per Monitor DPI no Windows Fall Creators Update (1709).](./media/office-dpi-behavior-on-windows-fall-creators-update.png)

### <a name="office-dpi-behavior-on-windows-april-2018-update-1803"></a><span data-ttu-id="e30fd-199">Comportamento DPI do Office no Windows (1803) de atualização de abril de 2018</span><span class="sxs-lookup"><span data-stu-id="e30fd-199">Office DPI behavior on Windows April 2018 Update (1803)</span></span>

<span data-ttu-id="e30fd-200">Com o Windows atualização de abril de 2018 (1803) e versões posteriores, DPI Office o comportamento de hospedagem usa DPI mista escala para alguns cenários.</span><span class="sxs-lookup"><span data-stu-id="e30fd-200">With Windows April 2018 (1803) update and later, The Office DPI hosting behavior uses mixed-mode DPI scaling for some scenarios.</span></span> <span data-ttu-id="e30fd-201">Isso permite que o sistema as janelas DPI cientes para ser os pais de definir por Monitor DPI cientes nas janelas do Office.</span><span class="sxs-lookup"><span data-stu-id="e30fd-201">This allows System DPI Aware windows to be parented to Office windows set to Per Monitor DPI aware.</span></span> <span data-ttu-id="e30fd-202">Isso ajuda a garantir a melhor compatibilidade quando o DPI é alterado quando os janelas estão bitmap alongada.</span><span class="sxs-lookup"><span data-stu-id="e30fd-202">This helps to ensure improved compatibility when the DPI changes when the windows are bitmap stretched.</span></span> <span data-ttu-id="e30fd-203">As janelas ainda podem ficar desfocadas de bitmap alongas.</span><span class="sxs-lookup"><span data-stu-id="e30fd-203">The windows might still be blurry from the bitmap stretching.</span></span>

![Diagrama mostrando janelas filho executando o sistema DPI cientes contexto no Windows abril de 2018 atualização (1803).](./media/office-dpi-behavior-on-windows-april-2018-update.png)

<span data-ttu-id="e30fd-205">Quando você cria um novo janelas filho, certifique-se de que elas correspondam às reconhecimento DPI da janela de seus pais.</span><span class="sxs-lookup"><span data-stu-id="e30fd-205">When you create new child windows, be sure they match the DPI awareness of their parent window.</span></span> <span data-ttu-id="e30fd-206">Você pode usar a função [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) para receber reconhecimento DPI da janela dos pais.</span><span class="sxs-lookup"><span data-stu-id="e30fd-206">You can use the [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) function to get the DPI awareness of the parent window.</span></span> <span data-ttu-id="e30fd-207">Para saber mais sobre DPI consistência de percepção, confira a seção "Forçada redefinição de reconhecimento DPI todo o processo" [desenvolvimento de aplicativos de área de trabalho DPI alto no Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span><span class="sxs-lookup"><span data-stu-id="e30fd-207">For more information about DPI awareness consistency, see the “Forced reset of process-wide DPI awareness” section in [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span></span>

> [!NOTE]
> <span data-ttu-id="e30fd-208">Você não pode depender reconhecimento de DPI o processo de como ela pode retornar [PROCESS_SYSTEM_DPI_AWARE](https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness) mesmo quando estiver o contexto de reconhecimento de conversa principal DPI aplicativo [DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="e30fd-208">You can’t rely on the Process DPI Awareness as it might return [PROCESS_SYSTEM_DPI_AWARE](https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness) even when the application main thread DPI awareness context is [DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context).</span></span> <span data-ttu-id="e30fd-209">Use a função [GetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext) Obtenha o contexto de reconhecimento de conversa DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-209">Use the [GetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext) function to get the thread DPI awareness context.</span></span>

## <a name="office-and-windows-dpi-compatibility-settings"></a><span data-ttu-id="e30fd-210">Configurações de compatibilidade do Office e Windows DPI</span><span class="sxs-lookup"><span data-stu-id="e30fd-210">Office and Windows DPI compatibility settings</span></span>

<span data-ttu-id="e30fd-211">Quando os usuários encontrarem suplementos ou soluções que estão sendo processados corretamente, algumas configurações de compatibilidade podem ajuda a corrigir o problema.</span><span class="sxs-lookup"><span data-stu-id="e30fd-211">When users encounter add-ins or solutions that are not rendering correctly, some compatibility settings can help correct the problem.</span></span>

<h3 id="office-compatibility"><span data-ttu-id="e30fd-212">Configurar o Office para otimizar para fins de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="e30fd-212">Configure Office to optimize for compatibility</span></span></h3>

<span data-ttu-id="e30fd-213">O Office tem uma configuração para otimizar para fins de compatibilidade quando mover para diferentes DPI escala em diferentes telas.</span><span class="sxs-lookup"><span data-stu-id="e30fd-213">Office has a setting to optimize for compatibility when moving to different DPI scales on different screens.</span></span> <span data-ttu-id="e30fd-214">O modo de compatibilidade desabilita os recursos de escala DPI para que todo o conteúdo no Office bitmap alongada quando movidas para uma exibição de uso de escala DPI diferentes.</span><span class="sxs-lookup"><span data-stu-id="e30fd-214">The compatibility mode disables DPI scaling so that everything in Office is bitmap stretched when moved to a display using different DPI scaling.</span></span> 

<span data-ttu-id="e30fd-215">O modo de compatibilidade força que o Office seja executado em modo Sistema DPI ciente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-215">The compatibility mode forces Office to run in System DPI aware mode.</span></span> <span data-ttu-id="e30fd-216">Isso faz com que janelas do aplicativo para esticar bitmap e pode ter um efeito de uma aparência desfocado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-216">This causes application windows to bitmap stretch and can have a side effect of a blurry appearance.</span></span> <span data-ttu-id="e30fd-217">Sua solução do Office não pode controlar essa configuração, como o usuário escolhe-lo.</span><span class="sxs-lookup"><span data-stu-id="e30fd-217">Your Office solution cannot control this setting because the user chooses it.</span></span> <span data-ttu-id="e30fd-218">Usar o modo de exibição de compatibilidade resolve a maioria dos problemas de desenho.</span><span class="sxs-lookup"><span data-stu-id="e30fd-218">Using the display compatibility mode solves most drawing problems.</span></span> <span data-ttu-id="e30fd-219">Para saber mais, confira [suporte do Office para alta definição exibe](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="e30fd-219">For more information, see [Office support for high definition displays](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span> 

### <a name="configure-windows-to-fix-blurry-apps"></a><span data-ttu-id="e30fd-220">Configurar o Windows para corrigir imagens desfocados aplicativos</span><span class="sxs-lookup"><span data-stu-id="e30fd-220">Configure Windows to fix blurry apps</span></span>

<span data-ttu-id="e30fd-221">Windows 10 (versão 1803) e tem uma configuração para corrigir aplicativos para que não estejam desfocados mais tarde.</span><span class="sxs-lookup"><span data-stu-id="e30fd-221">Windows 10 (Version 1803) and later has a setting to fix apps so they’re not blurry.</span></span> <span data-ttu-id="e30fd-222">Esta é outra configuração para fazer se a sua solução não processa corretamente.</span><span class="sxs-lookup"><span data-stu-id="e30fd-222">This is another setting to try if your solution is not rendering correctly.</span></span> <span data-ttu-id="e30fd-223">Sua solução do Office não pode controlar essa configuração, como o usuário escolhe-lo.</span><span class="sxs-lookup"><span data-stu-id="e30fd-223">Your Office solution cannot control this setting because the user chooses it.</span></span> <span data-ttu-id="e30fd-224">Para saber mais, confira [corrigir aplicativos que aparecem desfocados no Windows 10](https://support.microsoft.com/en-us/help/4091364/windows-10-fix-blurry-apps).</span><span class="sxs-lookup"><span data-stu-id="e30fd-224">For more information, see [Fix apps that appear blurry in Windows 10](https://support.microsoft.com/en-us/help/4091364/windows-10-fix-blurry-apps).</span></span>

## <a name="how-to-support-dpi-scaling-in-your-solution"></a><span data-ttu-id="e30fd-225">Como suporte a DPI sua solução de escala</span><span class="sxs-lookup"><span data-stu-id="e30fd-225">How to support DPI scaling in your solution</span></span>

<span data-ttu-id="e30fd-226">Algumas soluções, podem receber e responder às alterações DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-226">Some solutions can receive and respond to DPI changes.</span></span> <span data-ttu-id="e30fd-227">Alguns têm para solucionar esse problema se eles não podem receber notificações.</span><span class="sxs-lookup"><span data-stu-id="e30fd-227">Some have a workaround if they cannot receive notifications.</span></span> <span data-ttu-id="e30fd-228">A tabela a seguir lista os detalhes para cada tipo de solução.</span><span class="sxs-lookup"><span data-stu-id="e30fd-228">The following table lists the details for each solution type.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="e30fd-229">Tipo de solução</span><span class="sxs-lookup"><span data-stu-id="e30fd-229">Solution Type</span></span></th>
            <th><span data-ttu-id="e30fd-230">Tipo de janela</span><span class="sxs-lookup"><span data-stu-id="e30fd-230">Window type</span></span></th>
            <th><span data-ttu-id="e30fd-231">Pode responder a escala DPI</span><span class="sxs-lookup"><span data-stu-id="e30fd-231">Can respond to DPI scaling</span></span></th>
            <th><span data-ttu-id="e30fd-232">Mais detalhes</span><span class="sxs-lookup"><span data-stu-id="e30fd-232">More details</span></span></th>
        </tr>
    </thead>
<tbody>
    <tr>
        <td rowspan="2"><span data-ttu-id="e30fd-233"><a href="#vsto-add-ins">Suplementos VSTO</a></span><span class="sxs-lookup"><span data-stu-id="e30fd-233"><a href="#vsto-add-ins">VSTO Add-in</a></span></span></td>
        <td><span data-ttu-id="e30fd-234">Superior e seus descendentes</span><span class="sxs-lookup"><span data-stu-id="e30fd-234">Top and its descendants</span></span></td>
        <td><span data-ttu-id="e30fd-235">Sim</span><span class="sxs-lookup"><span data-stu-id="e30fd-235">Yes</span></span></td>
        <td><span data-ttu-id="e30fd-236">Ver <a href="#vsto-add-ins">orientações suplemento VSTO</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-236">See <a href="#vsto-add-ins">VSTO add-in guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="e30fd-237">Pais de filho na janela do Office</span><span class="sxs-lookup"><span data-stu-id="e30fd-237">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="e30fd-238">Não</span><span class="sxs-lookup"><span data-stu-id="e30fd-238">No</span></span></td>
        <td><span data-ttu-id="e30fd-239">Ver <a href="#office-compatibility">configurar o Office para otimizar a compatibilidade</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-239">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="e30fd-240"><a href="#custom-task-panes">painel de tarefas personalizado</a></span><span class="sxs-lookup"><span data-stu-id="e30fd-240"><a href="#custom-task-panes">Custom task pane</a></span></span></td>
        <td><span data-ttu-id="e30fd-241">Superior e seus descendentes</span><span class="sxs-lookup"><span data-stu-id="e30fd-241">Top and its descendants</span></span></td>
        <td><span data-ttu-id="e30fd-242">Sim</span><span class="sxs-lookup"><span data-stu-id="e30fd-242">Yes</span></span></td>
        <td><span data-ttu-id="e30fd-243">Ver <a href="#top-level-window-management">orientações de nível superior janela</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-243">See <a href="#top-level-window-management">top-level window guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="e30fd-244">Pais de filho na janela do Office</span><span class="sxs-lookup"><span data-stu-id="e30fd-244">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="e30fd-245">Não</span><span class="sxs-lookup"><span data-stu-id="e30fd-245">No</span></span></td>
        <td><span data-ttu-id="e30fd-246">Ver <a href="#office-compatibility">configurar o Office para otimizar a compatibilidade</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-246">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="e30fd-247"><a href="#com-add-ins">suplemento de COM</a></span><span class="sxs-lookup"><span data-stu-id="e30fd-247"><a href="#com-add-ins">COM Add-in</a></span></span></td>
        <td><span data-ttu-id="e30fd-248">Superior e seus descendentes</span><span class="sxs-lookup"><span data-stu-id="e30fd-248">Top and its descendants</span></span></td>
        <td><span data-ttu-id="e30fd-249">Sim</span><span class="sxs-lookup"><span data-stu-id="e30fd-249">Yes</span></span></td>
        <td><span data-ttu-id="e30fd-250">Ver <a href="#com-add-ins">Orientação de suplementos de COM</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-250">See <a href="#com-add-ins">COM Add-in guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="e30fd-251">Pais de filho na janela do Office</span><span class="sxs-lookup"><span data-stu-id="e30fd-251">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="e30fd-252">Não</span><span class="sxs-lookup"><span data-stu-id="e30fd-252">No</span></span></td>
        <td><span data-ttu-id="e30fd-253">Ver <a href="#office-compatibility">configurar o Office para otimizar a compatibilidade</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-253">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="e30fd-254"><a href="#activex-controls">Controle ActiveX</a></span><span class="sxs-lookup"><span data-stu-id="e30fd-254"><a href="#activex-controls">ActiveX control</a></span></span></td>
        <td><span data-ttu-id="e30fd-255">Superior e seus descendentes</span><span class="sxs-lookup"><span data-stu-id="e30fd-255">Top and its descendants</span></span></td>
        <td><span data-ttu-id="e30fd-256">Sim</span><span class="sxs-lookup"><span data-stu-id="e30fd-256">Yes</span></span></td>
        <td><span data-ttu-id="e30fd-257">Ver <a href="#activex-controls">orientações de controle ActiveX</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-257">See <a href="#activex-controls">ActiveX control guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="e30fd-258">Pais de filho na janela do Office</span><span class="sxs-lookup"><span data-stu-id="e30fd-258">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="e30fd-259">Sim</span><span class="sxs-lookup"><span data-stu-id="e30fd-259">Yes</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="e30fd-260"><a href="#web-add-ins">Suplemento da Web</a></span><span class="sxs-lookup"><span data-stu-id="e30fd-260"><a href="#web-add-ins">Web Add-in</a></span></span></td>
        <td><span data-ttu-id="e30fd-261">N/D</span><span class="sxs-lookup"><span data-stu-id="e30fd-261">NA</span></span></td>
        <td><span data-ttu-id="e30fd-262">Sim</span><span class="sxs-lookup"><span data-stu-id="e30fd-262">Yes</span></span></td>
        <td><span data-ttu-id="e30fd-263">Ver <a href="#web-add-ins">Orientações do suplemento Office</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-263">See <a href="#web-add-ins">Office web add-in guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="e30fd-264"><a href="#ribbon-extensibility">Extensão da faixa de opções</a></span><span class="sxs-lookup"><span data-stu-id="e30fd-264"><a href="#ribbon-extensibility">Ribbon extension</a></span></span></td>
        <td><span data-ttu-id="e30fd-265">NA</span><span class="sxs-lookup"><span data-stu-id="e30fd-265">NA</span></span></td>
        <td><span data-ttu-id="e30fd-266">NA</span><span class="sxs-lookup"><span data-stu-id="e30fd-266">NA</span></span></td>
        <td><span data-ttu-id="e30fd-267">Ver <a href="#ribbon-extensibility">Orientações de extensão da faixa de opções</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-267">See <a href="#ribbon-extensibility">Ribbon extension guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="e30fd-268"><a href="#ole">Cliente ou servidor OLE</a></span><span class="sxs-lookup"><span data-stu-id="e30fd-268"><a href="#ole">OLE server or client</a></span></span></td>
        <td><span data-ttu-id="e30fd-269">NA</span><span class="sxs-lookup"><span data-stu-id="e30fd-269">NA</span></span></td>
        <td><span data-ttu-id="e30fd-270">NA</span><span class="sxs-lookup"><span data-stu-id="e30fd-270">NA</span></span></td>
        <td><span data-ttu-id="e30fd-271">Ver <a href="#ole">diretrizes do cliente/servidor OLE</a>.</span><span class="sxs-lookup"><span data-stu-id="e30fd-271">See <a href="#ole">OLE server/client guidance</a>.</span></span></td>
    </tr>
</tbody>
</table>

<h3 id="vsto-add-ins"><span data-ttu-id="e30fd-272">Suplemento VSTO</span><span class="sxs-lookup"><span data-stu-id="e30fd-272">VSTO add-in</span></span></h3>

<span data-ttu-id="e30fd-273">O suplemento VSTO cria janelas filho que são pais de todas as janelas Office, verifique se corresponderem reconhecimento DPI da janela de seus pais.</span><span class="sxs-lookup"><span data-stu-id="e30fd-273">If your VSTO add-in creates child windows that are parented to any Office windows, be sure they match the DPI awareness of their parent window.</span></span> <span data-ttu-id="e30fd-274">Você pode usar a função [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) para receber reconhecimento DPI da janela dos pais.</span><span class="sxs-lookup"><span data-stu-id="e30fd-274">You can use the [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) function to get the DPI awareness of the parent window.</span></span> <span data-ttu-id="e30fd-275">Suas janelas filho não receberão notificações de alteração da DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-275">Your child windows will not get any DPI change notifications.</span></span> <span data-ttu-id="e30fd-276">Se a sua solução não processa corretamente, os usuários precisarão instalar o Office no modo de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="e30fd-276">If your solution is not rendering correctly, users will need to put Office into compatibility mode.</span></span>

<span data-ttu-id="e30fd-277">Para as janelas de nível superior que o suplemento VSTO cria, você pode configurá-los de qualquer modo de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-277">For any top-level windows your VSTO add-in creates, you can set them to any DPI awareness mode.</span></span> <span data-ttu-id="e30fd-278">O código de exemplo a seguir mostra como configurar o reconhecimento DPI desejado e como responder às alterações DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-278">The following sample code shows how to set up the desired DPI awareness, and how to respond to DPI changes.</span></span> <span data-ttu-id="e30fd-279">Você também precisará ajustar o app.config, conforme descrito no artigo [suporte a DPI alto nos formulários do Windows](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms).</span><span class="sxs-lookup"><span data-stu-id="e30fd-279">You will also need to adjust your app.config, as described in the [High DPI support in Windows Forms](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms) article.</span></span> 

```csharp
using System;
using System.Diagnostics;
using System.Drawing;
using System.Runtime.InteropServices;
using System.Windows.Forms;

namespace SharedModule
{
    // DpiAwareWindowsForm
    // For any top level winform you create, derive from the DpiWindowsForm class
    // if you are creating Windows Forms with the Dpi Awareness Context set to 
    // DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE or DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2
    //
    // For example, if you Window form class is defined as:
    //    public partial class TopLevelWinForm : Form
    //
    // update to:
    //    public partial class TopLevelWinForm : DpiAwareWindowsForm
    //
    // When showing the form, call SetThreadDpiAwarenessContext() or use a context block to
    // to set the desired Dpi Awareness Context.
    //
    // For example, here is code to show a Windows Form using a context block as Per Monitor Aware v2.
    //
    //    DPIContextBlock context = new DPIContextBlock(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2);
    //    TopLevelWinForm frm = new TopLevelWinForm();
    //    frm.Show();
    //
    public partial class DpiAwareWindowsForm : Form
    {
        private SizeF m_newDpi = SizeF.Empty;
        private SizeF m_oldDpi = SizeF.Empty;

        public DpiAwareWindowsForm()
        {
            this.HandleCreated += new EventHandler((sender, args) =>
            {
                m_oldDpi = m_newDpi = DPIHelper.GetDpiForWindowSizeF(this.Handle);
            });
        }

        public void OnDpiChangedEvent(RECT newRect)
        {
            this.SuspendLayout();

            // Resize form
            this.Width = newRect.Width;
            this.Height = newRect.Height;

            // Resize controls and set font sizes
            ScaleAllChildControls(this.Controls, m_oldDpi.Width, m_newDpi.Width);
            this.ResumeLayout(true);
        }

        // Additional changes may be needed for controls that set Anchor or Dock properties 
        private void ScaleAllChildControls(Control.ControlCollection controls, float oldDpi, float newDpi)
        {
            float scaleFactorChange = newDpi / oldDpi;

            foreach (Control control in controls)
            {
                control.Top = (int)(control.Top * scaleFactorChange);
                control.Left = (int)(control.Left * scaleFactorChange);
                control.Width = (int)(control.Width * scaleFactorChange);
                control.Height = (int)(control.Height * scaleFactorChange);
                control.Font = ScaleFont(control.Font, oldDpi, newDpi);
            }
        }

        private Font ScaleFont(Font font, float oldDpi, float newDpi)
        {
            float fontSizePx = 0.0f;
            float fontSizePt = 0.0f;

            fontSizePx = font.SizeInPoints / 72 * oldDpi;
            fontSizePt = fontSizePx * (newDpi / oldDpi) * 72 / oldDpi;

            return new Font(font.Name, fontSizePt, font.Style, GraphicsUnit.Point);
        }

        protected override void WndProc(ref Message m)
        {
            switch ((DPIHelper.WinMessages)m.Msg)
            {
                case DPIHelper.WinMessages.WM_DPICHANGED:
                    // Marshal the value in the lParam into a Rect.
                    RECT newDisplayRect = (RECT)Marshal.PtrToStructure(m.LParam, typeof(RECT));

                    // Remember current DPI and calculate current from WParam.
                    // Both X and Y are the same on Windows for Dpi.
                    m_oldDpi = m_newDpi;

                    m_newDpi.Width = (float)(m.WParam.ToInt32() >> 16);
                    m_newDpi.Height = (float)(m.WParam.ToInt32() & 0x0000FFFF);

                    // DPI should be the same for both width and height on Windows devices.
                    Debug.Assert(m_newDpi.Height == m_newDpi.Width);

                    if (m_oldDpi.Width != m_newDpi.Width)
                    {
                        OnDpiChangedEvent(newDisplayRect);
                    }
                    base.DefWndProc(ref m);
                    break;
                default:
                    base.WndProc(ref m);
                    break;
            }
        }
    }
}
```

<h3 id="custom-task-panes"><span data-ttu-id="e30fd-280">Painéis de Tarefas Personalizados</span><span class="sxs-lookup"><span data-stu-id="e30fd-280">Custom task panes</span></span></h3>

<span data-ttu-id="e30fd-281">Um painel de tarefas personalizados é criado como uma janela de filho pelo Office.</span><span class="sxs-lookup"><span data-stu-id="e30fd-281">A custom task pane is created as a child window by Office.</span></span> <span data-ttu-id="e30fd-282">Ao executar a atualização do Windows Fall Creators (1709), seu painel de tarefas será executado usando o mesmo modo reconhecimento DPI como o Office.</span><span class="sxs-lookup"><span data-stu-id="e30fd-282">When running on Windows Fall Creators Update (1709), your custom task pane will run using the same DPI awareness mode as Office.</span></span> <span data-ttu-id="e30fd-283">Ao executar o Windows (1803) de atualização de abril de 2018 e mais tarde, painel de tarefas será executada usando o modo de percepção DPI sistema.</span><span class="sxs-lookup"><span data-stu-id="e30fd-283">When running on Windows April 2018 Update (1803) and later, your custom task pane will run using System DPI awareness mode.</span></span> 

<span data-ttu-id="e30fd-284">Como painéis de tarefas personalizados são janelas filhos, elas não podem receber notificações de DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-284">Because custom task panes are child windows, they cannot receive DPI notifications.</span></span> <span data-ttu-id="e30fd-285">Se ele estiver desenhando incorretamente, o usuário será preciso usar [modo de compatibilidade do Office DPI](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="e30fd-285">If they are drawing incorrectly, the user will need to use [Office DPI compatibility mode](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>
<span data-ttu-id="e30fd-286">Se o painel de tarefas cria janelas de nível superior, essas janelas podem ser executadas em qualquer modo de percepção DPI e receber notificações de alteração DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-286">If your custom task pane creates top-level windows, those windows can run in any DPI awareness mode and receive DPI change notifications.</span></span> <span data-ttu-id="e30fd-287">Para saber mais, confira a seção deste artigo [gerenciamento de nível superior de janelas](#top-level-window-management).</span><span class="sxs-lookup"><span data-stu-id="e30fd-287">For more information, see the [Top-level window management](#top-level-window-management) section in this article.</span></span>

<h3 id="com-add-ins"><span data-ttu-id="e30fd-288">Suplemento COM</span><span class="sxs-lookup"><span data-stu-id="e30fd-288">COM add-ins</span></span></h3>

<span data-ttu-id="e30fd-289">O suplemento que cria janelas de nível superior podem receber notificações de DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-289">COM add-ins that create top-level windows can receive DPI notifications.</span></span> <span data-ttu-id="e30fd-290">Você deverá criar um [bloquear contexto](#build-a-context-block-for-incoming-thread-calls) para definir o reconhecimento DPI desejado para a janela da conversa, em seguida, criar sua janela.</span><span class="sxs-lookup"><span data-stu-id="e30fd-290">You should create a [context block](#build-a-context-block-for-incoming-thread-calls) to set the thread to the DPI awareness that you want for your window, then create your window.</span></span> <span data-ttu-id="e30fd-291">Há muito a manipulação notificações DPI corretamente, portanto, não deixe de ler [desenvolvimento de aplicativos de área de trabalho DPI alto no Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e30fd-291">There’s a lot to handling the DPI notifications correctly, so be sure to read [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics) for more details.</span></span>

<span data-ttu-id="e30fd-292">As [WM_DPICHANGED](https://docs.microsoft.com/windows/desktop/hidpi/wm-dpichanged) mensagem é enviada quando DPI uma janela foi alterado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-292">The [WM_DPICHANGED](https://docs.microsoft.com/windows/desktop/hidpi/wm-dpichanged) message is sent when the DPI for a window has changed.</span></span>  <span data-ttu-id="e30fd-293">Código não gerenciado, esta mensagem é tratada o [procedimento janela](https://docs.microsoft.com/windows/desktop/winmsg/using-window-procedures) para o HWND.</span><span class="sxs-lookup"><span data-stu-id="e30fd-293">In unmanaged code, this message is handled by the [Window Procedure](https://docs.microsoft.com/windows/desktop/winmsg/using-window-procedures) for the HWND.</span></span>  <span data-ttu-id="e30fd-294">Exemplo DPI alterar identificador código pode ser encontrado na WM_DPICHANGED artigo.</span><span class="sxs-lookup"><span data-stu-id="e30fd-294">Sample DPI change handler code can be found in the WM_DPICHANGED article.</span></span> 

<span data-ttu-id="e30fd-295">O suplemento que mostra janela filho que são pais de uma janela do Office não podem receber notificações de DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-295">COM add-ins that show child windows that are parented to a window in Office cannot receive DPI notifications.</span></span> <span data-ttu-id="e30fd-296">Se ele estiver desenhando incorretamente, o usuário será preciso usar [modo de compatibilidade do Office DPI](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="e30fd-296">If they are drawing incorrectly, the user will need to use [Office DPI compatibility mode](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>

<h3 id="activex-controls"><span data-ttu-id="e30fd-297">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="e30fd-297">ActiveX controls</span></span></h3>

<span data-ttu-id="e30fd-298">Como suporte a controles ActiveX de escala DPI depende se o controle é com janela ou sem janelas.</span><span class="sxs-lookup"><span data-stu-id="e30fd-298">How to support DPI scaling in ActiveX controls depends on whether the control is windowed or windowless.</span></span>

#### <a name="windowed-activex-controls"></a><span data-ttu-id="e30fd-299">Controles ActiveX em janelas</span><span class="sxs-lookup"><span data-stu-id="e30fd-299">Windowed ActiveX controls</span></span>

<span data-ttu-id="e30fd-300">Controles ActiveX em janelas recebem uma mensagem WM_SIZE sempre que no controle será redimensionado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-300">Windowed ActiveX controls receive a WM_SIZE message each time the control is resized.</span></span>  <span data-ttu-id="e30fd-301">Quando este evento é disparado, o código de manipulador de eventos pode ligar para o [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) função usar HWND do controle para obter a DPI calcular as diferenças de fator de escala e ajustar conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="e30fd-301">When this event is triggered, the event handler code can call the [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) function using the HWND of the control to get the DPI, calculate the scale factor differences, and adjust as needed.</span></span> 

<span data-ttu-id="e30fd-302">O exemplo a seguir permite um controle ActiveX com base MFC para responder a **OnSize** evento.</span><span class="sxs-lookup"><span data-stu-id="e30fd-302">The following example enables an MFC-based ActiveX control to respond to the **OnSize** event.</span></span> 

```cpp
void ChangeWindowFontDPI(HWND hWnd, UINT dpi) 
{ 
LOGFONT fontInfo1 = { 0 }; 
// Calculate the font height based on the DPI. 
fontInfo1.lfHeight = -MulDiv(DESIRED_HEIGHT, dpi, 72); 
fontInfo1.lfQuality = CLEARTYPE_QUALITY; 
wcscpy_s(fontInfo1.lfFaceName, DESIRED_FONT_NAME); 
 
::SendMessage(hWnd, WM_SETFONT, (WPARAM)::CreateFontIndirectW(&fontInfo1), TRUE); 
} 
 
BOOL CALLBACK CMainDialog::EnumChildProc(HWND hWnd, LPARAM lParam) 
{ 
CMainDialog* _this = (CMainDialog*) lParam; 
if (_this != nullptr) 
{ 
// Calculate the scale factor difference between the old and new DPI changes. 
double scale = (((double) _this->m_newDPI) /  
   (((double) _this->m_currentDPI) / 100.0)) / 100; 
 
RECT rect = {}; 
::GetWindowRect(hWnd, &rect); 
 
POINT pt = { rect.left, rect.top }; 
::ScreenToClient(::GetParent(hWnd), &pt); 
 
// Adjust the window based on the scale changes. 
::MoveWindow(hWnd, 
pt.x * scale, 
pt.y * scale, 
(rect.right - rect.left) * scale, 
(rect.bottom - rect.top) * scale, 
TRUE); 
 
ChangeWindowFontDPI(hWnd, _this->m_newDPI); 
return TRUE; 
} 
return FALSE; 
} 
 
void CMainDialog::OnSize(UINT nType, int cx, int cy) 
{ 
CDialog::OnSize(nType, cx, cy); 
 
// Get the new DPI and enumerate the child windows that will use that value. 
m_currentDPI = ::GetDpiForWindow(this->GetSafeHwnd()); 
::EnumChildWindows(this->GetSafeHwnd(), EnumChildProc, (LPARAM)this); 
} 
```

#### <a name="windowless-activex-controls"></a><span data-ttu-id="e30fd-303">Sem janela controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="e30fd-303">Windowless ActiveX controls</span></span>

<span data-ttu-id="e30fd-304">Sem janela de controles ActiveX, não há garantia tem um HWND.</span><span class="sxs-lookup"><span data-stu-id="e30fd-304">Windowless ActiveX controls are not guaranteed have an HWND.</span></span>  <span data-ttu-id="e30fd-305">Quando um controle ActiveX é inserido em uma tela de documento, ele é inserido no modo de design.</span><span class="sxs-lookup"><span data-stu-id="e30fd-305">When an ActiveX control is inserted onto a document canvas, it is put into design mode.</span></span>  <span data-ttu-id="e30fd-306">Em aplicativos do Office, hospedagem contêiner retornará 0 para ligar para hDC -> GetWindow() na: OnDraw evento quando o controle está no modo design.</span><span class="sxs-lookup"><span data-stu-id="e30fd-306">In Office applications, the hosting container will return 0 for the call to hDC->GetWindow() in the ::OnDraw event when the control is in design mode.</span></span>  <span data-ttu-id="e30fd-307">Não é possível recuperar uma DPI confiável nesse caso.</span><span class="sxs-lookup"><span data-stu-id="e30fd-307">A reliable DPI cannot be retrieved in this case.</span></span> 

<span data-ttu-id="e30fd-308">No entanto, quando o controle no modo de tempo de execução Office retornará HWND onde o controle é desenhar.</span><span class="sxs-lookup"><span data-stu-id="e30fd-308">However, when the control is in runtime mode, Office will return the HWND where the control is to be drawn.</span></span>  <span data-ttu-id="e30fd-309">Nesse caso, o desenvolvedor de controle pode ligar [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) e a atual fontes DPI e escala, controles e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e30fd-309">In this case, the control developer can call [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) and get the current DPI and scale fonts, controls, and so on.</span></span> 

<h3 id="ribbon-extensibility"><span data-ttu-id="e30fd-310">Extensibilidade da faixa de opções personalizada</span><span class="sxs-lookup"><span data-stu-id="e30fd-310">Custom ribbon extensibility</span></span></h3>

<span data-ttu-id="e30fd-311">Os retornos de chamadas do Office para controles de faixa de opções personalizada estará em um reconhecimento de conversa DPI do sistema ciente DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-311">Any callbacks from Office for custom ribbon controls will be in a DPI thread awareness of System DPI aware.</span></span>  <span data-ttu-id="e30fd-312">Se a sua solução estiver esperando um reconhecimento de conversa DPI diferentes, você deve implementar um bloco de contexto para configurar o reconhecimento de conversa conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="e30fd-312">If your solution is expecting a different DPI thread awareness, you should implement a context block to set the thread awareness as expected.</span></span> <span data-ttu-id="e30fd-313">Para saber mais, confira [criar um bloco contexto](#build-a-context-block-for-incoming-thread-calls).</span><span class="sxs-lookup"><span data-stu-id="e30fd-313">For more information, see [Build a context block](#build-a-context-block-for-incoming-thread-calls).</span></span>

<h3 id="ole"><span data-ttu-id="e30fd-314">Servidores e clientes OLE</span><span class="sxs-lookup"><span data-stu-id="e30fd-314">OLE clients and servers</span></span></h3>

<span data-ttu-id="e30fd-315">Quando um servidor OLE estiver hospedado em um contêiner de cliente OLE, você no momento não poderá fornecer informações de DPI atuais, nem tem suportadas.</span><span class="sxs-lookup"><span data-stu-id="e30fd-315">When an OLE server is hosted within an OLE client container, you currently can’t provide current or supported DPI information.</span></span> <span data-ttu-id="e30fd-316">Isso pode causar problemas como algumas combinações de pais para janela filho de modos misturado não têm suporte a arquitetura atual do Windows.</span><span class="sxs-lookup"><span data-stu-id="e30fd-316">This can cause problems because some combinations of parent to child window mixed modes are not supported by the current Windows architecture.</span></span> <span data-ttu-id="e30fd-317">Se o Word ou Excel detectar que há vários monitores com escalas de DPI diferentes, não serão compatíveis ativação in-loco.</span><span class="sxs-lookup"><span data-stu-id="e30fd-317">If Word or Excel detect that there are multiple monitors with different DPI scales, they will not support in-place activation.</span></span> <span data-ttu-id="e30fd-318">Seu servidor OLE será ativado fora do local.</span><span class="sxs-lookup"><span data-stu-id="e30fd-318">Your OLE server will activate out-of-place.</span></span> <span data-ttu-id="e30fd-319">Se você estiver tendo problemas com as interações de servidor OLE, o usuário será preciso usar [modo de compatibilidade do Office DPI](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="e30fd-319">If you are experiencing issues with OLE server interactions, the user will need to use [Office DPI compatibility mode](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>

<h3 id="web-add-ins"><span data-ttu-id="e30fd-320">Suplemento do Office Web</span><span class="sxs-lookup"><span data-stu-id="e30fd-320">Office Web Add-ins</span></span></h3>

<span data-ttu-id="e30fd-321">Suplementos do Office criados usando a API JavaScript do Office executam no controle do navegador.</span><span class="sxs-lookup"><span data-stu-id="e30fd-321">Office Add-ins built using the Office JavaScript API run inside a browser control.</span></span> <span data-ttu-id="e30fd-322">Você pode lidar com conjunto de escala DPI usando as mesmas técnicas usadas em qualquer design do aplicativo web.</span><span class="sxs-lookup"><span data-stu-id="e30fd-322">You can handle DPI scaling using the same techniques used in any web app design.</span></span> <span data-ttu-id="e30fd-323">Muitos recursos online estão disponíveis para ajudar a criar uma página da web para telas de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="e30fd-323">Many online resources are available to help design a web page for high resolution screens.</span></span>

## <a name="verify-that-your-solution-supports-dpi-scaling"></a><span data-ttu-id="e30fd-324">Verificar se a sua solução dá suporte a DPI escala</span><span class="sxs-lookup"><span data-stu-id="e30fd-324">Verify that your solution supports DPI scaling</span></span>

<span data-ttu-id="e30fd-325">Depois de atualizar o aplicativo para dar suporte a escala DPI, você deve validar suas alterações em um ambiente combinado DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-325">After you have updated your application to support DPI scaling, you should validate your changes in a mixed-DPI environment.</span></span> <span data-ttu-id="e30fd-326">Valide que o código de interface do usuário responde adequadamente a alterações DPI das janelas de sua solução são movidos de uma exibição para outro que tenha valores DPI diferentes.</span><span class="sxs-lookup"><span data-stu-id="e30fd-326">Validate that your UI code responds properly to DPI changes when your solution’s windows are moved from one display to another that has different DPI values.</span></span> <span data-ttu-id="e30fd-327">Confira mais informações sobre testes de técnicas de escala DPI [desenvolvimento de aplicativos de área de trabalho DPI alto no Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span><span class="sxs-lookup"><span data-stu-id="e30fd-327">For more information about DPI scaling testing techniques, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span></span>

<span data-ttu-id="e30fd-328">Você também pode encontrar essas técnicas adicionais úteis:</span><span class="sxs-lookup"><span data-stu-id="e30fd-328">You might also find these additional techniques helpful:</span></span>

- <span data-ttu-id="e30fd-329">Com um laptop, você poderá definir o monitor principal para um monitor externo e desencaixar laptop.</span><span class="sxs-lookup"><span data-stu-id="e30fd-329">With a laptop, you can set the primary monitor to an external monitor, then undock the laptop.</span></span> <span data-ttu-id="e30fd-330">Isso forçará o monitor principal para alterar para exibição laptop.</span><span class="sxs-lookup"><span data-stu-id="e30fd-330">This will force the primary monitor to change to the laptop display.</span></span>
- <span data-ttu-id="e30fd-331">Use Abrir fonte [WinSpy + + ferramenta](https://github.com/BissetJ/winspy/releases) para ajudar a depurar.</span><span class="sxs-lookup"><span data-stu-id="e30fd-331">Use the open source [WinSpy++ tool](https://github.com/BissetJ/winspy/releases) to help debug.</span></span> <span data-ttu-id="e30fd-332">Você pode usá-lo para ver a configuração de percepção DPI de qualquer janela.</span><span class="sxs-lookup"><span data-stu-id="e30fd-332">You can use it to see the DPI awareness setting of any window.</span></span>
- <span data-ttu-id="e30fd-333">Você pode usar área de trabalho remota para testar a vários monitores em um computador remoto selecionando Usar meus monitores para uma sessão remota na guia Exibir, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e30fd-333">You can use remote desktop to test multiple monitors on a remote computer by selecting Use all my monitors for the remote session on the Display tab, as shown in the following screenshot.</span></span>

![Aplicativo de Conexão de área de trabalho remoto mostrando a guia Exibir e selecionar usar meu monitores para sessão remota.](./media/remote-desktop-use-all-monitors.png)

## <a name="see-also"></a><span data-ttu-id="e30fd-335">Confira também</span><span class="sxs-lookup"><span data-stu-id="e30fd-335">See also</span></span>

### <a name="articles"></a><span data-ttu-id="e30fd-336">Artigos</span><span class="sxs-lookup"><span data-stu-id="e30fd-336">Articles</span></span>

- <span data-ttu-id="e30fd-337">O [desenvolvimento de um aplicativo WPF de reconhecimento de DPI por monitor](https://docs.microsoft.com/windows/desktop/hidpi/declaring-managed-apps-dpi-aware) fornece uma visão geral e um guia para escrever aplicativos da área de trabalho Win32.</span><span class="sxs-lookup"><span data-stu-id="e30fd-337">[Developing a Per-Monitor DPI-Aware WPF Application](https://docs.microsoft.com/windows/desktop/hidpi/declaring-managed-apps-dpi-aware) provides a general overview and guide for writing Win32 desktop applications.</span></span> <span data-ttu-id="e30fd-338">Muitas das mesmas técnicas descritas neste artigo se aplicará a soluções de extensibilidade do Office.</span><span class="sxs-lookup"><span data-stu-id="e30fd-338">Many of the same techniques described in this article will apply to Office extensibility solutions.</span></span>
- <span data-ttu-id="e30fd-339">
  [Escala de DPI mista e APIs de DPI](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-improvements-for-desktop-applications) tem uma lista de APIs relacionados para DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-339">[Mixed-Mode DPI Scaling and DPI-aware APIs](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-improvements-for-desktop-applications) has a list of APIs related to DPI.</span></span>
- <span data-ttu-id="e30fd-340">[Desenvolvedor guia: visualização por Monitor DPI - WPF ](https://github.com/Microsoft/WPF-Samples/blob/master/PerMonitorDPI/Developer%20Guide%20-%20Per%20Monitor%20DPI%20-%20WPF%20Preview.docx) abrange o guia de desenvolvimento de aplicativos WPF para criar reconhecimento de DPI WPF aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e30fd-340">[Developer Guide - Per Monitor DPI - WPF Preview](https://github.com/Microsoft/WPF-Samples/blob/master/PerMonitorDPI/Developer%20Guide%20-%20Per%20Monitor%20DPI%20-%20WPF%20Preview.docx) covers the WPF app development guide for building DPI-aware WPF apps.</span></span>
- <span data-ttu-id="e30fd-341">[Suporte do Office para alta definição exibe](https://support.office.com/article/Office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d) fornecer informações sobre como um usuário pode configurar o Office para otimizar para fins de compatibilidade se a sua solução do Office não tem suporte corretamente quando há alterações da DPI.</span><span class="sxs-lookup"><span data-stu-id="e30fd-341">[Office support for high definition displays](https://support.office.com/article/Office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d) provides information about how a user can set Office to optimize for compatibility if your Office solution is not supported properly when the DPI changes.</span></span>
- <span data-ttu-id="e30fd-342">[Exibir as alterações de dimensionamento para a atualização de aniversário do Windows 10](https://blogs.technet.microsoft.com/askcore/2016/08/16/display-scaling-changes-for-the-windows-10-anniversary-update/) é apresentar a uma postagem de blog sobre alterações com a atualização de aniversário do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e30fd-342">[Display Scaling changes for the Windows 10 Anniversary Update](https://blogs.technet.microsoft.com/askcore/2016/08/16/display-scaling-changes-for-the-windows-10-anniversary-update/) is a blog post that covers changes introduce with the Windows 10 Anniversary update.</span></span> 
- <span data-ttu-id="e30fd-343">[Alça DPI_AWARENESS_CONTEXT](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context) dispõe sobre valores DPI_AWARENESS_CONTEXT e definições de programação.</span><span class="sxs-lookup"><span data-stu-id="e30fd-343">[DPI_AWARENESS_CONTEXT handle](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context) has programming details on the DPI_AWARENESS_CONTEXT values and definitions.</span></span>
- <span data-ttu-id="e30fd-344">[Desenvolvimento de aplicativos de área de trabalho DPI alto no Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#testing-your-changes) inclui informações sobre testes da seção de testar suas alterações.</span><span class="sxs-lookup"><span data-stu-id="e30fd-344">[High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#testing-your-changes) includes information about testing in the Testing Your Changes section.</span></span>

### <a name="code-samples"></a><span data-ttu-id="e30fd-345">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="e30fd-345">Code samples</span></span>

- [<span data-ttu-id="e30fd-346">Exemplo de DPI percepção por janela</span><span class="sxs-lookup"><span data-stu-id="e30fd-346">Per-window DPI Awareness sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow)
- [<span data-ttu-id="e30fd-347">Exemplo DPI dinâmico</span><span class="sxs-lookup"><span data-stu-id="e30fd-347">Dynamic DPI sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DynamicDPI)
- [<span data-ttu-id="e30fd-348">Exemplo de WPF cientes por Monitor</span><span class="sxs-lookup"><span data-stu-id="e30fd-348">Per-Monitor Aware WPF sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
