# mekotools/etherpad — Spiegel des amtlichen Etherpad-Abbilds

Dieses Repository baut **nichts**. Es spiegelt ausschliesslich das amtliche
Abbild des Etherpad-Projekts, digest-genagelt, nach
`ghcr.io/mekotools/etherpad`.

- Quelle: `docker.io/etherpad/etherpad@sha256:6f87beef31d91e4a44c7e3fe64043dd294f70443a80267a77267bdac704819a1`
- Fassung: `3.3.7` (Etikett `3.3.7`, dazu `latest`)
- Werkzeug-Projekt: <https://github.com/ether/etherpad> (Apache-2.0)
- Spiegel-Ablauf: `.github/workflows/spiegel.yml` (`docker pull` -> `docker tag` -> `docker push`)

Der Push geschieht **aus diesem Repository heraus**; nur so ist das Paket mit
einem oeffentlichen Repository verknuepft und ohne Anmeldung ziehbar.

Der Digest des gespiegelten Manifests weicht vom Quell-Digest ab: `docker push`
schreibt die Manifest-Form um. Inhaltlich gleich sind `config.digest` und die
Schichtenliste (Nachweis im Werkzeug-Repository `mekotools/mekotools-etherpad`,
Datei `docs/abbild.md`).
