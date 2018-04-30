# ssb-identities

manage multiple ssb identities, as an sbot plugin.

## api

## identities.main (cb)

returns the main identity (sbot.id)

## identities.list (cb)

returns the list of identities, with the main
identity first.

## identities.create (cb)

create a new identity, stored in `~/.ssb/identities/secret_[N].butt`
where N is the left-padded number of this identity.
returns the id of the newly created identity.

## identities.publishAs({id:id, content: obj, private: boolean}, cb) 

publish a message as a specific identity.
`id` must be provided and must be already in
the identities list. If `private` is true,
`content.recps` must be set. `recps` must contain
the `id`.

## License

MIT

