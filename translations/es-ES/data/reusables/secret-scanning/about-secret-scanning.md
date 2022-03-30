Si alguien registra un secreto de un socio de {% data variables.product.company_short %} en un repositorio {% if currentVersion == "free-pro-team@latest" %}público o privado{% endif %} de {% data variables.product.product_name %}, el {% data variables.product.prodname_secret_scanning %} captura el secreto de acuerdo a como se haya registrado y te ayuda a mitigar el impacto de la fuga. Se notifica a los administradores de repositorio sobre cualquier confirmación que contenga un secreto y pueden ver rápidamente todos los secretos en la pestaña de seguridad de éste.