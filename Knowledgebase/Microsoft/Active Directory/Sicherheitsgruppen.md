
**Enterprise Admins**
- sind eine AD-Sicherheitsgruppe in der Stammdomäne der Active Directory-Gesamtstruktur.
- Gruppenmitglieder verfügen über vollständige Berechtigungen für jede Domäne in der AD Gesamtstruktur (standardmäßig). Diese Berechtigung kommt durch die Mitgliedschaft in der integrierten Sicherheitsgruppe Administratoren auf den DCs einer jeden Domäne in der Gesamtstruktur zustande.
- Sie haben administrative Berechtigungen zur Durchführung von gesamtstrukturweiten Änderungen bspw. dem Hinzufügen und Entfernen von Domänen sowie dem Herstellen von Vertrauensbeziehungen zwischen Domänen.
- Standardmäßig ist das einzige Mitglied der AD-Sicherheitsgruppe das Administratorkonto für die Stammdomäne der Gesamtstruktur.

**Domain Admins**
- ist eine globale AD-Sicherheitsgruppe, deren Mitglieder zur Verwaltung der Domäne autorisiert sind.
- sind Mitglied der integrierten Sicherheitsgruppe Administratoren auf jedem Host, der der Domäne beigetreten ist (Standardkonfiguration). Dadurch besitzen sie administrative Berechtigungen auf allen Hosts innerhalb der Domäne.
- Domänen-Admins enthält ausschließlich das RID500-Konto der Domäne und Break-Glass-Konten als Mitglieder.

**Schema Admins**
- Eine universale AD-Sicherheitsgruppe in der Stammdomäne der Gesamtstruktur, mit den Änderungen am Active Directory-Schema der Gesamtstruktur möglich sind.
- Das einzige Mitglied der AD-Sicherheitsgruppe ist das Administratorkonto der Stammdomäne (standardmäßig).
- In der Regel hält die AD-Sicherheitsgruppe keine Mitglieder. Sie wird ausschließlich befüllt, wenn Anpassungen am Active Directory-Schema durchgeführt werden sollen. Danach kann die AD-Sicherheitsgruppe wieder geleert werden.

**Administrators**
- Mitglieder dieser AD-Sicherheitsgruppe haben die volle Kontrolle über alle Domain Controller in der Domäne
- Wird über Active Directory-Verzeichnis-Replizierung zwischen den Domain Controllern übertragen.
- Standardmäßig sind die Gruppen „Domain Admins“, „Enterprise Admins“ und das RID500-Domänenadministratorkonto Mitglieder der AD-Sicherheitsgruppe „Administrators“ im Active Directory.
