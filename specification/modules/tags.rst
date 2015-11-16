Room Tagging
============

.. _module:tagging:

Users can add tags to rooms. Tags are short strings used to label rooms, e.g.
"work", "family". A room may have multiple tags. Tags are only visible to the
user that set them but are shared across all their devices.

Events
------

The tags on a room are received as single ``m.tag`` event in the
``private_user_data`` section of a room in a v2 /sync.

The ``m.tag`` can also be received in a v1 /events response or in the
``private_user_data`` section of a room in v1 /initialSync. ``m.tag``
events appearing in v1 /events will have a ``room_id`` with the room
the tags are for.

Each tag has an associated JSON object with information about the tag, e.g how
to order the rooms with a given tag.

{{m_tag_event}}

Client Behaviour
----------------

{{v2_tags_http_api}}