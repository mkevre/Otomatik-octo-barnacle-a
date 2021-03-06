---
title: Configurar métodos de recuperação da autenticação de dois fatores
intro: Você pode configurar vários métodos de recuperação para acessar sua conta em caso de perda das credenciais da autenticação de dois fatores.
redirect_from:
  - /articles/downloading-your-two-factor-authentication-recovery-codes
  - /articles/setting-a-fallback-authentication-number
  - /articles/about-recover-accounts-elsewhere
  - /articles/adding-a-fallback-authentication-method-with-recover-accounts-elsewhere
  - /articles/generating-and-storing-an-account-recovery-token
  - /articles/configuring-two-factor-authentication-recovery-methods
  - /github/authenticating-to-github/configuring-two-factor-authentication-recovery-methods
  - /github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication-recovery-methods
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - 2FA
shortTitle: Configurar recuperação de 2FA
---

Além de armazenar com segurança os códigos de recuperação da autenticação de dois fatores, é enfaticamente recomendável configurar um ou mais métodos adicionais de recuperação.

## Baixar os códigos de recuperação da autenticação de dois fatores

{% data reusables.two_fa.about-recovery-codes %} Você também pode baixar os códigos de recuperação a qualquer momento depois de habilitar a autenticação de dois fatores.

Para manter sua conta protegida, não compartilhe nem distribua seus códigos de recuperação. É recomendável salvá-los com um gerenciador de senhas seguro, como o:
- [1Password](https://1password.com/)
- [LastPass](https://lastpass.com/)

Em caso de geração de novos códigos de recuperação ou desabilitação e reabilitação da 2FA, os códigos nas configurações de segurança serão atualizados automaticamente.

{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.security %}
{% data reusables.two_fa.show-recovery-codes %}
4. Salve os códigos de recuperação em um local seguro. Seus códigos de recuperação podem ajudar você a ter acesso novamente à sua conta no caso de perda do acesso.
    - Para salvar os códigos de recuperação no dispositivo, clique em **Download** (Baixar).
    - Para salvar uma cópia impressa dos códigos de recuperação, clique em **Print** (Imprimir).
    - Para copiar os códigos de recuperação para armazenamento em um gerenciador de senhas, clique em **Copy** (Copiar). ![Lista de códigos de recuperação com opção para baixar, imprimir ou copiar os códigos](/assets/images/help/2fa/download-print-or-copy-recovery-codes-before-continuing.png)

## Gerar um conjunto de códigos de recuperação

Depois que você usa um código de recuperação para voltar a ter acesso à sua conta, ele não pode ser reutilizado. Se os 16 códigos de recuperação já foram usados, você pode gerar outra lista de códigos. Gerar um novo conjunto de códigos de recuperação invalidará outros códigos gerados anteriormente.

{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.security %}
{% data reusables.two_fa.show-recovery-codes %}
3. Para criar outro branch de códigos de recuperação, clique em **Generate new recovery codes** (Gerar novos códigos de recuperação). ![Botão Generate new recovery codes (Gerar novos códigos de recuperação)](/assets/images/help/2fa/generate-new-recovery-codes.png)

## Configurar uma chave de segurança como um método adicional da autenticação de dois fatores

Você pode configurar uma chave de segurança como um método secundário da autenticação de dois fatores e usá-la para voltar a ter acesso à sua conta. Para obter mais informações, consulte "[Configurar autenticação de dois fatores](/articles/configuring-two-factor-authentication#configuring-two-factor-authentication-using-a-security-key)".

{% ifversion fpt or ghec %}

## Configurar um número de autenticação de fallback

É possível fornecer um segundo número para um dispositivo de fallback. Se você perder acesso ao dispositivo principal e aos códigos de recuperação, um número de SMS de backup pode ajudar a acessar a sua conta.

Você pode usar um número de fallback, independentemente de ter configurado a autenticação por mensagem de texto ou aplicativo móvel TOTP.

{% warning %}

**Aviso:** usar um número de fallback é o último recurso. É recomendável configurar métodos de recuperação adicionais no de caso de definir um número de autenticação de fallback.
- Invasores podem atacar as operadores de celular, colocando a autenticação por SMS em risco.
- As mensagens SMS são aceitas somente em determinados países fora dos EUA; para obter uma lista, consulte "[Países onde a autenticação por SMS é aceita](/articles/countries-where-sms-authentication-is-supported)".

{% endwarning %}

{% data reusables.user-settings.access_settings %}
{% data reusables.user-settings.security %}
3. Ao lado de "Fallback SMS number" (Número para SMS do fallback), clique em **Add** (Adicionar). ![Botão Add fallback SMS number (Adicionar número para SMS do fallback)](/assets/images/help/2fa/add-fallback-sms-number-button.png)
4. Em "Fallback SMS number" (Número para SMS do fallback), clique em **Add fallback SMS number** (Adicionar número para SMS do fallback). ![Texto Adicionar número para SMS do fallback](/assets/images/help/2fa/add_fallback_sms_number_text.png)
5. Selecione o código do seu país e digite o número do celular, incluindo o código de área. Confirme se as informações estão corretas e clique em **Set fallback** (Definir fallback). ![Definir número para SMS do fallback](/assets/images/help/2fa/2fa-fallback-number.png)

Após a configuração, o dispositivo de backup receberá um SMS de confirmação.

{% endif %}

## Leia mais

- [Sobre a autenticação de dois fatores](/articles/about-two-factor-authentication)"
- "[Configurar a autenticação de dois fatores](/articles/configuring-two-factor-authentication)"
- "[Acessar o {% data variables.product.prodname_dotcom %} usando a autenticação de dois fatores](/articles/accessing-github-using-two-factor-authentication)"
- "[Recuperar sua conta se você perder as credenciais da autenticação de dois fatores](/articles/recovering-your-account-if-you-lose-your-2fa-credentials)"
